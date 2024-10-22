---
title: CloudSim学习
slug: cloudsim-learning-z16jgio
url: /post/cloudsim-learning-z16jgio.html
date: '2023-05-05 20:13:28+08:00'
lastmod: '2024-10-22 10:40:01+08:00'
toc: true
tags:
  - 教程
keywords: 教程
isCJKLanguage: true
---

# CloudSim学习

# CloudSim相关情况

* [CloudSim ](https://www.cloudsimtutorials.online/cloudsim/)是什么？

  * 一个模拟工具包，支持云核心功能的建模和模拟。
  * 是[墨尔本大学](http://www.unimelb.edu.au/)​[计算机科学和软件工程系](http://www.csse.unimelb.edu.au/)的[云计算和分布式系统 （CLOUDS） 实验室](http://cloudbus.org/)开发的
  * Coud Sim最经典的入门版本是3.0.3（需要额外配置math库），从3.0到5.0都可以基于传统的jdk1.8，但最近的6.0（beta）有<span data-type="text" style="color: var(--b3-font-color5);">大规模的改动</span>，<span data-type="text" style="color: var(--b3-font-color5);">有大量语法糖</span>，只能基于jdk11和jdk17。

    * **3.0.3版本**主要做的是任务单虚拟机，虚拟机到物理机的映射  
      下载地址：[Releases · Cloudslab/cloudsim](https://github.com/Cloudslab/cloudsim/releases)
    * 改动内容：

      * 4.0支持了容器虚拟化
      * 5.0加入了更多的场景比如虚拟机性能监控、多云的Web应用程序建模，软件定义网络（SDN）/服务功能链（SFC）等
      * 6.0 beta更多的改动在于语法上（废弃jdk8，加入了jdk11/17的语法糖），但介绍里没有提到过微服务（项目和changelog都全局检索过microservice，但没有匹配，**大致**排除隐含的情况）
* **相关平台**

  * [CloudSim: a toolkit for modeling and simulation of cloud computing environments and evaluation of resource provisioning algorithms - Calheiros - 2011 - Software: Practice and Experience - Wiley Online Library](https://onlinelibrary.wiley.com/doi/abs/10.1002/spe.995)
  * [Cloudslab/cloudsim：CloudSim：云计算基础设施和服务建模和仿真框架 (github.com)](https://github.com/Cloudslab/cloudsim)

    * [CLOUDS的github主页](https://github.com/Cloudslab)
  * [The CLOUDS Lab: Flagship Projects - Gridbus and Cloudbus](http://www.cloudbus.org/cloudsim/)  
    CLOUDS关于CLoudSim和其相关项目的介绍。
  * [Cloudsim – Cloudsim Tutorials](https://www.cloudsimtutorials.online/cloudsim/)

    * [文章](https://www.cloudsimtutorials.online/about-cloudsim-tutorials/)

      *  

        * [iFogsim Entities](https://www.cloudsimtutorials.online/ifogsim-entities/) – This article summarise various entity classes available in the iFogsim simulation toolkit and how it is directly related to the basic cloudsim simulation toolkit’s simulation engine.
        * [iFogsim Project Structure: A Beginners Guide](https://www.cloudsimtutorials.online/ifogsim-project-structure-a-beginners-guide/) – This article will serve as a guide to understanding the iFogSim project structure API toolkit. It is absolutely necessary to study the project namespaces to understand which type of classes exist and how they are grouped.
        * [Cloudsim ](https://www.cloudsimtutorials.online/cloudsim/)– Cloudsim is a simulation toolkit that supports the modeling and simulation of the core functionality of the cloud. This article discusses the overview of the cloudsim toolkit and helps you get started along with reference to the relevant resources and relevant cloudsim tutorials.
        * [CloudSim Setup using Eclipse](https://www.cloudsimtutorials.online/cloudsim-setup-using-eclipse/) – A Step by step Cloudsim tutorial guide to install/setup the Cloudsim Simulation Toolkit using Eclipse IDE. This Cloudsim setup tutorials start with the required prerequisites and takes you on the journey till the execution of your first example of Cloudsim.
        * [CloudSim Simulation Toolkit: An Introduction](https://www.cloudsimtutorials.online/cloudsim-simulation-toolkit-an-introduction/) – A must-read comprehensive article that will give an insight into the essential basics of the Cloudsim simulation toolkit, which is an important simulator tool for researchers working in the field of cloud computing.
        * [Virtual machine migration in Cloudsim](https://www.cloudsimtutorials.online/virtual-machine-migration-in-cloudsim/) – For cloud-based researchers, the article will help to appreciate the step by step process of Virtual Machine Migration implementation done in cloudsim.
        * [Create a user-defined event and CloudsimTags](https://www.cloudsimtutorials.online/create-a-user-defined-event-and-cloudsimtags/) – simulating user-defined event in cloudsim, is major requirements for the user scenario implementation and it crucial to define corresponding cloudsimtags.
        * [Cloudlet in Cloudsim Simulation](https://www.cloudsimtutorials.online/cloudlet-in-cloudsim-simulation/) – Cloudlet in cloudsim defines the attributes related to the workload which is to be simulated in simulation engine e.g. instruction length, resource, etc.
        * [Power-Aware Simulation Scenario in Cloudsim](https://www.cloudsimtutorials.online/guide-to-power-aware-simulation-scenario-in-cloudsim/) – Support of Power-aware Simulation scenario in cloudsim is one of the major breakthroughs and it has been widely utilized by the research community to publish their optimized results related to their proposed algorithms referring to VM migrations, SLA’s, resource allocation, reducing power consumption, etc.
        * [Guide to CloudsimExample1.java simulation workflow](https://www.cloudsimtutorials.online/guide-to-cloudsimexample1-java-simulation-workflow/) – This article will help you to understand the CloudsimExample1.java simulation workflow with a detailed discussion on the code of cloudsimexample1.java.
        * [Beginners Guide to Cloudsim Project Structure](https://www.cloudsimtutorials.online/beginners-guide-to-cloudsim-project-structure/) – This article is a beginner’s guide to get started with the cloudsim simulation toolkit. Before drilling down on code, it is essential to understand which namespace contains which type of classes and how they are grouped.
        * [How to do Virtual machine and Task Scheduling in CloudSim](https://www.cloudsimtutorials.online/how-to-do-virtual-machine-and-task-scheduling-in-cloudsim/) – In cloud computing, scheduling is an exciting topic. The cloudsim simulation toolkit framework has addressed this use case and provided a set of class hierarchy which specifies the basic scheduling mechanism w.r.t. The timeshare as well as spaceshare. This article explains regarding same and how it can be extended.
        * [ServiceSim: A Modelling and Simulation Toolkit of Microservice Systems in Cloud-Edge Environment](https://link.springer.com/chapter/10.1007/978-3-031-48421-6_18)
        * [EvolutionSim: An Extensible Simulation Toolkit for Microservice System Evolution](https://ieeexplore.ieee.org/abstract/document/10248295)
        * [CloudNativeSim: a toolkit for modeling and simulation of cloud-native applications](https://arxiv.org/abs/2409.05093)
    * [培训](https://www.cloudsimtutorials.online/cloudsim-training/)（要钱）
  * 学习资源

    * [Learn from a list of articles available on CloudsimTutorials.online](https://www.cloudsimtutorials.online/)
    * An online self-paced course named [Learn Basics of Cloudsim](https://www.superwitsacademy.online/essential-cloudsim-tutorials), with weekly content updates till August 2021.
    * [List of Research Work relates to Cloudsim](https://scholar.google.com/scholar?hl=en&as_sdt=2005&cites=272054103506592999&scipsc=&q=&scisbd=1)
* 环境需求与安装？

  * Java IDE、双核处理器、2 GB RAM 和 1 GB Memory
  * [CloudSim Setup using Eclipse – Cloudsim Tutorials](https://www.cloudsimtutorials.online/cloudsim-setup-using-eclipse/)
  * **3.0.3版本仍依赖commons-math-3-3.6.1.jar**  
    已将其打包好，回头会和pdf一起发群里
* **参考博客：**

  * [CloudSim 的详解与调度扩展实现-腾讯云开发者社区-腾讯云 (tencent.com)](https://cloud.tencent.com/developer/beta/article/1673805)

# 总体设计

**<u>CloudSim的8大功能</u>**（摘自CloudSim GitHub主页）

* support for modeling and simulation of large scale Cloud computing data centers （数据中心：是服务器、存储器、网络设备以及其他相关设备和系统的集成，旨在提供集中的计算和存储资源。）
* support for modeling and simulation of virtualized server hosts, with customizable policies for provisioning host resources to virtual machines（虚拟机&主机资源）
* support for modeling and simulation of application containers（容器）
* support for modeling and simulation of energy-aware computational resources（能量资源：主要指电力）
* support for modeling and simulation of data center network topologies and message-passing applications（网络拓扑和通信）
* support for modeling and simulation of federated clouds（联合云）
* support for dynamic insertion of simulation elements, stop and resume of simulation（模拟事件的动态插入）
* support for user-defined policies for allocation of hosts to virtual machines and policies for allocation of host resources to virtual machines（分配策略）

**<u>总结成一句：可以对大规模的云计算数据中心、虚拟机、容器、网络拓扑和联合云进行建模和模拟，支持自定义的各类资源分配和调度策略。</u>**

​![zotero_JU2fHGMJhS](assets/cloudsim架构图-20230925113341-4p4bokt.png)![zotero_yRvFrTfXxU](assets/cloudsim类图-20230925113550-pvy5e12.png)​

总体设计图（摘自cloudsim论文）

## cloudsim扩展和改进

* [cloudsim的扩展列表](http://www.cloudbus.org/cloudsim/)
* [CloudSim Automation](https://github.com/cloudsimplus/cloudsimplus-automation)  
  能够自动化读取yaml文件
* [CloudSimEx](https://github.com/Cloudslab/CloudSimEx)  
  一系列扩展的集合
* [cloudsimplus](https://github.com/cloudsimplus/cloudsimplus)  
  民间改进版，功能更全，支持java17+

## 思考：**DataCenter、VM、Host分别是怎么建模的？** 它们之间如何联动？各种策略如何起作用？

1. <span data-type="text" style="color: var(--b3-font-color9);">数据中心怎么建模的？</span>

    * 见创建DataCenterCharacteristic、创建DataCenter
    * 创建Broker，后续的vm、cloudlet都是提交给DataCenterBroker去代理执行的。
    * PEs（Processing Elements）指的是可以执行计算任务的单元，例如一个CPU核心。一个datacenter有多个pe，一个host也可以有多个。
    * PowerVmAllocationPolicyMigrationAbstract —— 一个模板类为了实现功率监控动态虚拟机整合算法，用于虚拟机在线迁移到动态再分配虚拟机在每次构件时。重写的主要方法是optimizeAllocation。
2. <span data-type="text" style="color: var(--b3-font-color9);">虚拟机是怎么建模的？</span>

    * 先指定ID（vmid）、处理速度（mips）、镜像大小（size）、内存（ram）、带宽（bw）、处理单元数量（pes_num）、虚拟机管理策略（vmm），然后创建VM类（加入vmList）并提交给Broker，创建VM
    * VM分配策略见**((20230509154911-im1gkas "VmAllocationPolicy类"))**
    * VM调度策略见**((20230510085728-dj27do5 "VmScheduler"))**  
      在一个单独主机上实现资源分配给虚拟机的算法
3. <span data-type="text" style="color: var(--b3-font-color9);">任务（cloudlet）是怎么建模的？</span>

    * 先指定ID（cloudlet_id）、指令条数（length）、输入和输出的规模（file_size、output_size）、利用率模型（utilizationModel），然后创建cloudlet对象并加入cloudletList，提交给Broker，具体见创建Cloudlet
    * 任务执行时间=任务长度/执行速度，即$T=MI/MIPS$

      * 如果一个虚拟机上同时运行多个任务，不论使用空间共享还是时间共享，  这些任务的执行时间是一定的（任务的总指令长度和虚拟机的执行速度是一定  的）
      * 如果一个任务在某个虚拟机上执行的时间最短，那么它在其他虚拟机上 的执行时间也是最短的。
      * 如果一个虚拟机的执行速度最快，那么它不论执行哪个任务都是最快的。
    * CloudLet调度策略见**((20230510085828-rk1hhrz 'CloudLetScheduler类'))**  
      在一个单独的虚拟机实现调度云任务的算法
4. <span data-type="text" style="color: var(--b3-font-color9);">物理机是怎么建模的？</span>

    * 先指定ID（host_id）、内存（ram）、主存（storage）、带宽（bw），然后创建host类并加入hostList，具体见创建host
5. <span data-type="text" style="color: var(--b3-font-color9);">1个User对应于1个broker，1个broker可以代理多个datacenter，1个datacenter拥有1个vm list、1个host list和多个pe list，每个host对应1个pe list，即可能有n个pe和m个vm，1个vm可能被分配到s个pe</span>（$m*s\le n$）

* VmAllocationPolicy类

  1. 在[CloudSim源码分析之虚拟机分配策略](http://blog.chinaunix.net/uid-29798642-id-4410294.html)博客中有详细的源码分析
  2. 含义：VmAllocationPolicy是一个抽象的类，它表示数据中心中主机对虚拟机的配置策略。它为放置虚拟机而分配主机。它支持保留主机的两阶段承诺：首先，我们保留主机，一旦用户承诺，它就被有效地分配给他/她。默认的静态策略是((20230509160617-lj1qjqj "VmAllocationPolicySimple"))。也可以通过实现optimizeAllocation方法来实现一个动态虚拟机再分配算法。
  3. 默认配置

      1. 定义关键变量

          1. ​`private Map<String, Host> vmTable;`​​​（虚拟机分配到主机的映射表）
          2. ​`private Map<String, Integer> usedPes;`​​​（vm占用了几个处理器核心）
          3. ​`private List<Integer> freePes;`​​​（记录每台主机可用的处理器核心数）
      2. 基于上述参数创建`VmAllocationPolicy`​​​`Simple`​​​​对象，代表着**vm调度策略**（将主机的资源分配给虚拟机）

          ```java
          public VmAllocationPolicy(List<? extends Host> list) {
          	super(list);

          	setFreePes(new ArrayList<Integer>());
          	for (Host host : getHostList()) {
          		getFreePes().add(host.getNumberOfPes());

          	}

          	setVmTable(new HashMap<String, Host>());
          	setUsedPes(new HashMap<String, Integer>());
          }
          ```
      3. 通过该对象其可以选择满足特定条件（内存、软件环境配置等）的主机来分配虚拟机，下面是默认的分配算法（对应`VmAllocationPolicySimple`​​​）

          ```java
          @Override
          public boolean allocateHostForVm(Vm vm) {
          	int requiredPes = vm.getNumberOfPes();
          	boolean result = false;
          	int tries = 0;
          	List<Integer> freePesTmp = new ArrayList<Integer>();
          	for (Integer freePes : getFreePes()) {
          		freePesTmp.add(freePes);
          	}//构造了临时的空闲Pe列表

          	if (!getVmTable().containsKey(vm.getUid())) { // 如果VmTable不包含对应Uid（即未创建成功）
          		do {// 持续尝试分配直到创建成功或遍历结束（找到合适的主机）
          			int moreFree = Integer.MIN_VALUE;// 当前最大可用核心数
          			int idx = -1; //当前最大可用核心数对应主机的下标

          			// 默认算法：从前往后遍历，大于MIN_VALUE既可调度，但不保证符合VM需求，所以效率较低
          			for (int i = 0; i < freePesTmp.size(); i++) {
          				if (freePesTmp.get(i) > moreFree) {
          					moreFree = freePesTmp.get(i);
          					idx = i;
          				}
          			}

          			Host host = getHostList().get(idx);
          			result = host.vmCreate(vm); //创建未必成功，需要判断

          			if (result) { // 如果vm在该主机成功创建，返回true
          				getVmTable().put(vm.getUid(), host);
          				getUsedPes().put(vm.getUid(), requiredPes);
          				getFreePes().set(idx, getFreePes().get(idx) - requiredPes);
          				result = true;
          				break;
          			} else { // 如果创建失败，将该pe资源也设为当前的最小值（相当于排除）
          				freePesTmp.set(idx, Integer.MIN_VALUE);
          			}
          			tries++;
          		} while (!result && tries < getFreePes().size());

          	}

          	return result;
          }

          @Override
          public boolean allocateHostForVm(Vm vm, Host host) {
          	if (host.vmCreate(vm)) { // if vm has been succesfully created in the host
          		getVmTable().put(vm.getUid(), host);

          		int requiredPes = vm.getNumberOfPes();
          		int idx = getHostList().indexOf(host);
          		getUsedPes().put(vm.getUid(), requiredPes);
          		getFreePes().set(idx, getFreePes().get(idx) - requiredPes);

          		Log.formatLine(
          				"%.2f: VM #" + vm.getId() + " has been allocated to the host #" + host.getId(),
          				CloudSim.clock());
          		return true;
          	}

          	return false;
          }
          ```
      4. 删除虚拟机相应的映射关系，通过主机销毁虚拟机并更新可用的处理器核心数

          ```java
          public void deallocateHostForVm(Vm vm) {
          	Host host = getVmTable().remove(vm.getUid());
          	int idx = getHostList().indexOf(host);
          	int pes = getUsedPes().remove(vm.getUid());
          	if (host != null) {
          		host.vmDestroy(vm);
          		getFreePes().set(idx, getFreePes().get(idx) + pes);
          	}
          }
          ```
* VmScheduler类

  1. 含义：VmScheduler是一个抽象类，它代表了虚拟机监控器（VMM）用于在主机中运行的虚拟机之间共享PM的处理能力的策略。每个主机都必须使用自己的VmScheduler实例，以便为在其上运行的虚拟机安排主机的PE分配。
  2. VmSchedulerTimeShared 和 VmSchedulerSpaceShared是指VMs在时间和空间上分用PEs资源
* CloudLetScheduler类

  * 汇总了关于设备属性和资源的相关函数，例如更新和获取资源列表、更新时间等

# **解释Examples**

​![CloudSim Example](assets/CloudSim%20Example-20230611172022-r8glqrd.png)​

1. Example1:  showing how to create **a data center** with **one** **host** and run ** one** **cloudlet** on it.

    1. 描述

        1. 初始化cloudism package：  
             `Cloudsim.init(num_user, calendar, trace_flag);`​​​​​​​​​​​​​​​​​
        2. 创建DataCenters：  
            ​`Datacenter datacenter0 = createDatacenter("`​​​​​​​​​​​​​​​​`name`​​​​​​​​​​​​​​​​​`");`​​​​​​​​​​​​​​​​​

            1. 创建hostList和peList：  
                ​`List<Host> hostList = new ArrayList<Host>()
                 List<Pe> peList = new ArrayList<Pe>()`​​​​​​​​​​​​​​​​​​​
            2. 指定mips（cpu处理速度）并分配给pe（Processor Elements，处理单元）

                ​`int mips = `​​​​​​​​​​​​​​​​​​`1000`​​​​​​​​​​​​​​​​​​​`; peList.add(new Pe(`​​​​​​​​​​​​​​​​​​​`id`​​​​​​​​​​​​​​​​​​​​`, new PeProvisionerSimple(mips))) `​​​​​​​​​​​​​​​​​​​
            3. 创建host

                ```java
                int hostId = 0;
                int ram = 2048; // host memory (MB)
                long storage = 1000000; // host storage
                int bw = 10000; // bandwidth

                hostList.add(
                new Host(
                	hostId,
                	new RamProvisionerSimple(ram),
                	new BwProvisionerSimple(bw),
                	storage,
                	peList,
                	new VmSchedulerTimeShared(peList)
                	)
                );
                ```
            4. 创建DatacenterCharacteristics（数据中心静态属性）对象来存储数据中心资源，比如体系结构，操作系统，主机列表，分配策略，时间或空间共享，时区，开销

                ```java
                String arch = "x86"; // system architecture
                String os = "Linux"; // operating system
                String vmm = "Xen"; // Virtual Machine Manager
                double time_zone = 10.0; // time zone this resource located
                double cost = 3.0; // the cost of using processing in this resource
                double costPerMem = 0.05; // the cost of using memory in this resource
                double costPerStorage = 0.001; // the cost of using storage in this
                								// resource
                double costPerBw = 0.0; // the cost of using bw in this resource
                LinkedList<Storage> storageList = new LinkedList<Storage>(); // we are not adding SAN
                // devices by now

                DatacenterCharacteristics characteristics = new DatacenterCharacteristics(arch, os, vmm, hostList, time_zone, cost, costPerMem,costPerStorage, costPerBw);
                ```
            5. 基于上述资源和架构生成Datacenter

                ```java
                Datacenter datacenter = null;
                try {
                	datacenter = new Datacenter(name, characteristics, new VmAllocationPolicySimple(hostList), storageList, 0);
                } catch (Exception e) {
                	e.printStackTrace();
                }

                return datacenter;
                ```
        3. 创建Broker（服务代理商）：  
            ​`DatacenterBroker broker = createBroker();
             int brokerId = broker.getId();`​​​​​​​​​​​​​​​​​
        4. 创建并描述VM，然后提交给broker：

            ```java
            vmlist = new ArrayListvm();`
            // VM description
            int vmid = 0;
            int mips = 1000;
            long size = 10000; // image size (MB)
            int ram = 512; // vm memory (MB)
            long bw = 1000;
            int pesNumber = 1; // number of cpus
            String vmm = "Xen"; // VMM name

            // create VM
            Vm vm = new Vm(vmid, brokerId, mips, pesNumber, ram, bw, size, vmm, new CloudletSchedulerTimeShared());

            // add the VM to the vmList
            vmlist.add(vm);

            // submit vm list to the broker
            broker.submitVmList(vmlist);
            ```
        5. 创建Cloudlet（任务单元）并提交给broker：

            ```java
            cloudletList = new ArrayList<Cloudlet>();

            // Cloudlet properties（给单元分配资源）
            int id = 0;
            long length = 400000; //the length or size (in MI) of this cloudlet to beexecuted in a PowerDatacenter
            long fileSize = 300; //输入
            long outputSize = 300; //输出
            UtilizationModel utilizationModel = new UtilizationModelFull();
            //下面传入了三次utilizationModel，分别代表cpu、ram、bw的工具模块
            Cloudlet cloudlet = new Cloudlet(id, length, pesNumber, fileSize, outputSize, utilizationModel, utilizationModel, utilizationModel);
            cloudlet.setUserId(brokerId);
            cloudlet.setVmId(vmid);

            // add the cloudlet to the list
            cloudletList.add(cloudlet);

            // submit cloudlet list to the broker
            broker.submitCloudletList(cloudletList);
            ```
        6. 启动Simulation：

            ```java
            CloudSim.startSimulation();

            CloudSim.stopSimulation();
            ```
        7. 打印结果：  
            ​`List<Cloudlet> newList = broker.getCloudletReceivedList();
            printCloudletList(newList);`​​​​​​​​​​​​​​​​​

            ```java
            private static void printCloudletList(List<Cloudlet> list) {
            	int size = list.size();
            	Cloudlet cloudlet;

            	String indent = "    ";
            	Log.printLine();
            	Log.printLine("========== OUTPUT ==========");
            	Log.printLine("Cloudlet ID" + indent + "STATUS" + indent
            			+ "Data center ID" + indent + "VM ID" + indent + "Time" + indent
            			+ "Start Time" + indent + "Finish Time");

            	DecimalFormat dft = new DecimalFormat("###.##");
            	for (int i = 0; i < size; i++) {
            		cloudlet = list.get(i);
            		Log.print(indent + cloudlet.getCloudletId() + indent + indent);

            		if (cloudlet.getCloudletStatus() == Cloudlet.SUCCESS) {
            			Log.print("SUCCESS");

            			Log.printLine(indent + indent + cloudlet.getResourceId()
            					+ indent + indent + indent + cloudlet.getVmId()
            					+ indent + indent
            					+ dft.format(cloudlet.getActualCPUTime()) + indent
            					+ indent + dft.format(cloudlet.getExecStartTime())
            					+ indent + indent
            					+ dft.format(cloudlet.getFinishTime()));
            		}
            	}
            }
            ```
    2. ​![idea64_DXXeQ9s2P9](assets/idea64_DXXeQ9s2P9-20230925121655-gv87eng.png)​
2. Example2:  A simple example showing how to create ** a datacenter with one host ** and run ** two cloudlets ** on it.（with **same MIPS ** requirements）

    1. 描述

        1. ```java
            //3.0.3本主要做任务单虚拟机，所以需要两个vm，下同	
            Vm vm1 = new Vm(vmid, brokerId, mips, pesNumber, ram, bw, size, vmm, new CloudletSchedulerTimeShared());
            vmid++;
            Vm vm2 = new Vm(vmid, brokerId, mips, pesNumber, ram, bw, size, vmm, new CloudletSchedulerTimeShared());
            //add the VMs to the vmList
            vmlist.add(vm1);
            mlist.add(vm2);
            //submit vm list to the broker
            broker.submitVmList(vmlist);

            UtilizationModel utilizationModel = new UtilizationModelFull();

            Cloudlet cloudlet1 = new Cloudlet(id, length, pesNumber, fileSize, outputSize, utilizationModel, utilizationModel, utilizationModel);
            cloudlet1.setUserId(brokerId);
            id++;
            Cloudlet cloudlet2 = new Cloudlet(id, length, pesNumber, fileSize, outputSize, utilizationModel, utilizationModel, utilizationModel);
            cloudlet2.setUserId(brokerId);
            //add the cloudlets to the list
            cloudletList.add(cloudlet1);
            cloudletList.add(cloudlet2);
            //submit cloudlet list to the broker
            broker.submitCloudletList(cloudletList);
            ```
    2. ​![image](assets/image-20230509223529-ep0uck5.png)​

        资源量相同则时长相同
3. Example3: A simple example showing how to create **a datacenter with** **two hosts** and run **two cloudlets** on it.（with **different MIPS** requirements）

    1. 描述

        1. 同上，只是创建vm时给了不同的mips、hostList里有两个host（分别给了不同的peList）、cloudletList里有两个cloudlet
    2. ​![image](assets/image-20230509223409-34yykvp.png)
4. Example4: A simple example showing how to create **two datacenters** **with one host each** and run **two cloudlets** on them.

    1. ​![image](assets/image-20230509225730-gc11k3a.png)​

        同上，只是创建了两次DataCenter
5. Example5: A simple example showing how to create **two datacenters with one host each** and run cloudlets of **two users** on them.

    1. ​![image](assets/image-20230509225450-xl4anvz.png)​

        num_user=2，除了hostList，其它（DataCenter、vm、cloudlet）都弄两份，基本同上
6. Example6: An example showing how to create **scalable simulations**.（可扩展的模拟，可反复创建vm和cloudlet）

    1. ​![image](assets/image-20230925142651-gds19t3.png)​

        当一台虚拟机上执行多条cloudlet时，由于时分复用的原则，会一起执行完毕，并返回总共的执行时间
7. Example7: An example showing how to **pause and resume the simulation**, and create simulation entities (a DatacenterBroker in this example) **dynamically**.（暂停和恢复）

    1. 描述：

        1. 主线程开始，创建并启动一个监视线程，然后休眠1秒，之后开始模拟。与此同时，监视线程尝试在模拟时钟到达200单位时暂停模拟，并在模拟暂停期间执行一些任务，如创建和提交虚拟机和云任务。完成这些任务后，监视线程请求恢复模拟。
        2. **创建并启动监视线程**:`new Thread(monitor).start();`​  
            这行代码创建了一个新线程，使用先前定义的 `monitor`​（即实现了 `Runnable`​ 接口的对象）作为其执行任务。然后这个新线程开始运行。在这个线程中，它会尝试等待模拟时钟到达200单位时暂停模拟并创建新的任务，在时钟到达之前主线程会继续执行。
        3. **主线程休眠**:`Thread.sleep(1000);`​  
            我猜测这里是让主线程休眠1000毫秒（1秒），为刚才启动的minitor线程提供了时间来尝试暂停模拟。（注释掉也不会影响结果）
        4. **启动模拟**:`CloudSim.startSimulation();`​  
            在休眠结束后，两个线程会挨个调用 `CloudSim.startSimulation()`​ 来启动模拟。
8. Example8: An example showing how to create simulation entities (a DatacenterBroker in this example) **in run-time** using **a global manager entity** (**GlobalBroker**).（在运行时创建模拟实体）

    1. 值得注意的是，提交仍然用了最初的datacenter的broker

‍

‍

```shell
	 * Updates processing of each cloudlet running in this PowerDatacenter. It is necessary because
	 * Hosts and VirtualMachines are simple objects, not entities. So, they don't receive events and
	 * updating cloudlets inside them must be called from the outside.
```
