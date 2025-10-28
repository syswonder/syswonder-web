# Syswonder Open Source Projects

## hvisor

![](../_media/hvisor-logo.svg )

hvisor is a separation kernel hypervisor implemented in Rust language.
It is highly simplified and optimized for time and space partitioning.
It is a light-weight type-1 hypervisor, and partitions resources into
zones. Each zone has an appliance, may it be Linux, RTOS, Unikernel,
baremetal app, etc. Zone0 is reserved for management purpose, a
management Linux appliance provides tool for managing other zones. 

The hvisor design references much from [jailhouse](https://github.com/siemens/jailhouse).

<i class="fa-brands fa-github"></i> Repo: [https://github.com/syswonder/hvisor](https://github.com/syswonder/hvisor)

<i class="fa-solid fa-envelopes-bulk"></i> Mail list: [hypervisor@syswonder.org](https://maillist.syswonder.org/mailman3/lists/hypervisor.syswonder.org/)

## ruxos

![](../_media/ruxos-logo.svg)

ruxos is a [Unikernel](https://en.wikipedia.org/wiki/Unikernel) operating system, supporting Linux applications. ruxos is inspired by [ArceOS](https://github.com/rcore-os/arceos). ArceOS defines a set of interfaces among different os modules. ruxos addes/optimizes/replaces necessary modules to meet the requirements of different ubiquitous applications. Ruxos is developped in type-safe Rust language. 

<i class="fa-brands fa-github"></i> Repo: [https://github.com/syswonder/ruxos](https://github.com/syswonder/ruxos)

<i class="fa-solid fa-envelopes-bulk"></i> Mail list: [unikernel@syswonder.org](https://maillist.syswonder.org/mailman3/lists/unikernel.syswonder.org/)

## Robonix

<img src="../_media/robonix-logo.svg" width=400>

Robonix is an operating system designed for embodied artificial intelligence (EAI), an AI paradigm based on embodied cognition that emphasizes the collaboration between brain and body through a closed-loop perception–planning–action cycle. A key question here is: How should the “brain” of EAI be constructed and operated so that machines can truly realize this concept?

Recent approaches, such as Vision-Language-Action (VLA) models and World Models, focus mainly on AI models themselves. We argue that building an EAI “brain” also requires system-level support for model development, deployment, execution, and management. Robonix addresses this need by providing a cross-heterogeneous hardware foundation, enabling robots to acquire new skills and perform tasks efficiently.

Robonix decouples AI models from hardware, treating them as executable programs to support “train once, deploy anywhere” portability. Its Perception–Connection–Cognition–Control service framework addresses common challenges in perception, understanding, planning, action, and environmental interaction.
By simplifying the construction of intelligent robot brains and promoting the co-evolution of software and hardware ecosystems, Robonix aims to make embodied AI robots more capable, adaptable, and user-friendly.

<i class="fa-brands fa-github"></i> Repo: [https://github.com/syswonder/robonix](https://github.com/syswonder/robonix)

<i class="fa-solid fa-envelopes-bulk"></i> Mail list: [robotos@syswonder.org](https://maillist.syswonder.org/mailman3/lists/robotos.syswonder.org/)


