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

