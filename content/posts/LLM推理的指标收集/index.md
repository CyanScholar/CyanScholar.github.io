---
title: "LLM推理过程的指标收集方式（总结）"
date: 2024-02-21
draft: true
tags: ["LLM","推理"]
category: "博客"
series: ["LLM推理"]
series_order: 1
---

**我们大致可以将收集方式分成三类：**

**最主要的区别是对各个指标的定义的区别，例如Nvidia中[GenAI-Perf对性能指标的定义](https://docs.nvidia.com/nim/benchmarking/llm/latest/metrics.html)，或者**

### 一、在client端收集

**代表**：[llm-perf](https://github.com/ray-project/llmperf)、[GenAI-Perf](https://docs.nvidia.com/deeplearning/triton-inference-server/user-guide/docs/perf_analyzer/genai-perf/README.html)

**原理**：当采用**流式传输**时，client端可以通过记录发送请求和收到tokens的时间戳来收集TTFT、ITL、e2e_latency，自然也就能推算出TPOT和throughput等。但这样的方式里，TTFT会包含token编解码的时间和一些server的启动时间，而ITL不会包含

**特点**：

1. 这种方式可以不影响serve端代码，但是指标的结果可能没那么精确，因为需要做de-tokenization，而且不同工具对于ITL的**定义不一致**。
2. 除了收集perf指标外，这类工具往往也集成了**load test功能（基本上都是复现或者直接使用 [Locust](https://locust.io/) and [K6](https://k6.io/)）**和**compatibal APIs（如OpenAI的API，[etc.](https://www.notion.so/API-1a18b4ca4e0881488065ccc550d922eb?pvs=21)）**。

当然，我们也可以自己实现这些东西，只要采用了流式传输，这些都很简单。

### 二、在server端收集

**代表**：vllm、我自己写的[包装器](https://gist.github.com/CyanScholar/c99aeb25be0dad184360e9fb0d9ba407)

**原理**：这里记录两种方式
1. 通过给forward函数进行**包装**，可以追踪记录model级别或者layer级别的性能。这种方式不会更改模型代码，但需要确保包装是在最上层的。
2. 直接修改LLM的代码，例如写一个CustomLM，继承LLaMAforCausalLM，然后在内部修改即可。这种方式可能会更改模型代码，但也可以自定义实现很多其他功能，适合自定义系统。

**特点**：这种方式可以做到更为**精确**，可以直接获取TPOT，也不强求流式传输的机制。但这种方式耦合比较严重，适合系统内部集成（例如vllm）。

### 三、在kernel层面收集

**代表**：nsight compute、pytorch profiler、nsight profiler...（这种一般都叫“xxx profiler”）

**原理**：追踪算子并将其数据收集到一个数据库，例如ncu是sqlite，然后再渲染数据库到dashboard。（更具体的我也不那么清楚）
**特点**：粒度足够细，信息很全面，但是渲染和插叙也很慢。

### 四、在cluster层面收集
**代表**：DCGM
**特点**：
- 支持与k8s体系配合，支持exporter、grafana、OpenTelemetry等等。
- 需要集群的root权限，否则一些指标如SM Activity获取不到。