# Syswonder: Exploring New OS for In-situ Computing

Syswonder is an open-source community spontaneously formed by a group of
system software enthusiasts. It is dedicated to exploring new operating
system technologies for future ubiquitous intelligent computing
scenarios, especially in-situ computing.

## In-situ computing

In-situ computing refers to performing computing near the data source in
order to perceive the field environment and cognize the on-site
situation in real-time, and take action promptly. In-situ computing
applications typically run on asymmetric multi-processor SoC platforms
integrating heterogeneous processors like MCU, CPU, NPU, TPU, FPGA, and
DSP. Based on these platforms, in-situ computing tasks should be able to
perform intelligent computing on multi-source and
multi-modal sensing data in real-time.  Intelligent driving, smart
industry, unmanned systems, and medical devices are typical in-situ
computing scenarios.

In-situ computing tasks are complex and varied, involving the mixed
operation of real-time, reliable tasks and high-performance
tasks, as well as the collaboration of deterministic computing tasks and
probabilistic inference tasks. Moreover, in-situ computing tasks are
usually specialized, requiring the system to have good software-defined
adaptation and dynamic optimization capabilities, posing new challenges
for operating systems.

Take unmanned systems as an example, which typically have two main units:
the control unit and the mission unit. The control unit is responsible
for controlling the movement of the unmanned system, while the mission
unit interacts with the outside world and processes sensed data on-site to
make decisions promptly. These two functional units have
different demands on the operating system: the control unit requires
high real-time assurance and functional safety, whereas the mission
unit demands high computational capability and fault tolerance from
the operating system. Traditionally, engineers often use two different
computers to perform these two different functions. Now, unmanned systems
are rapidly transitioning to using a central computer, most of the time
of AMP architecture, to perform all these tasks. However, most current
operating systems fail to meet the needs of such in-situ computing on
this kind of AMP platform. We need a new operating system.

## Syswonder Community's Research on Operating Systems for In-situ Computing

At the current stage, the main goal of the Syswonder community is to
conduct research on new ubiquitous operating systems for in-situ
computing. This research focuses on new end devices based on AMP SoCs
and supports mixed deployment of real-time and non-real-time tasks, as
well as deterministic computing tasks and probabilistic inference tasks.
The research spans operating system architecture, kernel mechanisms,
safety assurance, and application support.

### Design Philosophy

#### #1 Operating Systems for In-situ Computing Should be Specialized

In most in-situ computing scenarios, only a limited number of the computational tasks are deployed and perform special missions, which means the operating system should be specialized, not general
purpose.

An important design philosophy of general-purpose operating systems like
Linux maximizes the usage of hardware resources by improving the system
throughput. To achieve this, Linux has made numerous complex and
sophisticated designs around resource sharing, including various
concurrency, synchronization, and scheduling mechanisms. Its monolithic
kernel architecture delivers outstanding performance and offers
excellent support for traditional CPUs like Symmetric Multi-Processing (SMP) and Non-Uniform Memory Access (NUMA), making it
dominant in many general-purpose computing fields such as servers, data
centers, and networks, particularly suited for high-performance
computing tasks.

However, Linux's design aimed at high throughput makes it unsuitable for
running real-time tasks. Real-time tasks require predictable system
behavior, emphasizing the deterministic and timeliness of task latency.
**PREEMPT_RT** is a set of Linux kernel patches that support real-time
tasks, but as of 2024, **PREEMPT_RT** has not been incorporated into
the mainline Linux kernel.

On the hardware side, many embedded systems adopt asymmetric
heterogeneous multi-processor (AMP) designs. To support heterogeneous
multi-processors, Linux provides the **remoteproc** and **RPmsg** frameworks,
allowing RTOS applications to run on remote heterogeneous processors.
However, the **remoteproc** framework does not effectively isolate RTOS
applications from other applications, presenting significant security
risks, and making it unsuitable for safety-critical scenarios.

Various real-time operating systems (RTOS) are mostly specialized,
primarily ensuring real-time characteristics but offering poor support for
general-purpose computing tasks.

Therefore, for in-situ computing, the Syswonder community proposes the
following design rationale that combines the strengths of both RTOS and
Linux:

- Simplify processor management by statically assigning processors to applications according to requirements and minimizing dynamic scheduling;

- Simplify task management by allowing tasks to exclusively possess processors and computing resources, minimizing concurrency, and avoiding resource contention as much as possible. 

#### #2 Operating systems for in-situ computing should be highly safe

Many in-situ computing scenarios are safety-critical, and the operating
system kernel itself should be highly safe and reliable.

Here, safety primarily means the correctness of the system's functions.

The Syswonder community intends to ensure functional safety through two
approaches:

- Utilizing the type-safe Rust language for system implementation, which can significantly enhance memory safety compared to the C language. 

- Applying formal verification measures to core code to ensure consistency between the implementation and the specification. 

#### #3 Operating systems for in-situ computing should be highly intelligent

Many in-situ computing applications involve executing AI probabilistic inference tasks, such as intrusion detection, pattern recognition, defect
detection, as well as the complex recognition of field situations by
computing aggregation on multi-source, multi-modal sensed data on-site.
These scenarios require the operating system to provide strong support
for AI probabilistic inference tasks.

The Syswonder community plans to make AI probabilistic inference
services a core part of the operating system, providing native support
for AI tasks based on AI chips.

### Syswonder little.BIG Dual-kernel Architecture

Based on the above requirements and design philosophy, the
Syswonder community, inspired by ideas from separation kernel and
unikernel designs, proposes the **little.BIG** dual-kernel
architecture. This architecture aims to optimize resource management and
application performance in asymmetric multi-processor systems. In this
dual-kernel architecture:

- **little Kernel**: This kernel is responsible for managing the
  system's hardware resources, with the design goals of being lightweight,
  safe, and efficient. Acting as a small manager, it undertakes the
  duties of allocating and isolating system resources, ensuring the
  security and stability of the system. The **little** kernel partitions
  physical resources into different zones based on the application
  requirements, ensuring temporal and spatial separation of each zone,
  thus providing an isolated and independent runtime environment for
  applications. A zone's resources can be physical hardware or virtual resources. In implementation, the
  **little** kernel can be an extremely lightweight Type 1 Hypervisor,
  running at a high privilege level such as ARM's EL2. 

- **BIG Kernel**: This type of kernel is specifically responsible for
  application support, with the design goals centered around robustness and
  flexibility. Acting as a big supporter, it provides rich application
  interfaces and an efficient runtime environment to meet complex and
  diverse application needs. The **BIG kernel** and its applications
  run within the zones provided by the **little kernel**, exclusively
  utilizing the resources of the corresponding zone. The **BIG kernel** and its
  applications are referred to as an **appliance**, which can be a
  unikernel operating system like RuxOS supporting a single application,
  or a Linux operating system supporting multiple applications or an
  RTOS for real-time applications, or even bare-metal programs. 

Through the collaboration of the **little** and **BIG** kernels, the
**little.BIG** architecture can meet the requirements of in-situ
computing applications.  Additionally, it maintains good compatibility
with existing Linux and RTOS ecosystems.

![](../_media/overview.svg)

### Current Projects

- A lightweight Type 1 hypervisor, [hvisor](https://github.com/syswonder/hvisor), primarily follows the [separation kernel](https://en.wikipedia.org/wiki/Separation_kernel) concept and
  serves as the **little** kernel in the **little.BIG** dual-kernel
  architecture. The main function of hvisor is to partition the system's
  physical resources into various zones. Through strict partitioning,
  hvisor ensures rigorous time and space isolation between zones,
  supporting the independent and interference-free operation of systems
  within each zone. The systems running within these partitions are
  referred to as appliances and often operate as lightweight virtual
  machines. Common appliances include standard Linux OS, Unikernel OS,
  Android OS, real-time RTOS, and even bare-metal applications. In
  the current design, zone0, also known as the root zone, is responsible for
  system management tasks. ZoneU typically handles high-computational
  tasks, with appliances that can be Unikernel OS or Linux OS; ZoneR is
  dedicated to real-time computing tasks, with appliances generally
  being RTOS running on MCUs. 

- A lightweight, unikernel operating system [RuxOS](https://github.com/syswonder/ruxos), compatible with Linux applications, primarily follows the [unikernel](https://en.wikipedia.org/wiki/Unikernel) design philosophy and serves as the
  **BIG** kernel in the **little.BIG** dual-kernel architecture.
  Considering that in edge ubiquitous computing scenarios, applications
  are usually limited in number and relatively fixed, RuxOS simplifies
  the operating system design to support only a single application. The
  kernel functions are provided as libraries, with the application running 
  directly in kernel mode. This library-style operating system
  significantly enhances application performance, while security
  concerns are primarily addressed by the underlying Type 1 hypervisor
  (hvisor).

- A set of operating system foundational components implemented in Rust,
  such as file systems, network protocol stacks, memory managers, and
  message communication mechanisms. These components can be used to
  build specific library operating systems.

## Future Vision

We believe that the future will be an era of ubiquitous intelligent
computing, characterized by the ternary fusion of human society,
cyberspace, and the physical world, where there will be numerous smart
devices that are ubiquitous and unnoticeable. Each smart device will
have a brain-like computer that performs various tasks for the device.
Just as every human individual is unique, the brain-like computer of
each smart device will also be unique, with specific hardware carriers,
working scenarios, and task missions.  Therefore, each brain-like
computer should have a specific operating system tailored to its
customized needs. We can call this brain-like computer **ubiquitous computer**.
The Syswonder community hopes to provide ubiquitous operating
systems(UOS) for brain-like computer in smart devices, exploring the
future of software-defined ubiquitous operating systems for smart
devices.

|                  | Desktop Computer             | Mobile Computer                | Ubiquitous Computer      |
| ---------------- | ---------------------------- | ------------------------------ | ---------------------------- |
| Key Technology   | CPU + Internet               | Low-power CPU + Mobile Network | AI Chip + Ubiquitous Network |
| Instruction Set  | x86                          | ARM                            | RISC-V                       |
| HCI              | GUI                          | Touch                          | Multi-modal                  |
| Computing Model  | Deterministic Computing      | Deterministic Computing        | Probabilistic Inference      |
| Application Form | Algorithms + Data Structures | Algorithms + Data Structures   | Models + Strategies          |
| Operating System | Windows, Linux               | iOS, Android                   | UOS             |
