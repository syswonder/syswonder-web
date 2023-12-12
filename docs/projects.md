# 矽望开源项目

## hvisor

Rust实现的Type-1虚拟机监视器（Hypervisor），采用基于基础构件的可重构设计思想，主要提供硬件资源虚拟化、分区安全隔离的能力。hvisor的设计借鉴了[jailhouse](https://github.com/siemens/jailhouse)。

项目地址: [https://github.com/syswonder/hvisor](https://github.com/syswonder/hvisor) 

邮件列表: [hypervisor@syswonder.org](https://maillist.syswonder.org/mailman3/lists/hypervisor.syswonder.org/)

## ruxos

ruxos是单一内核操作系统[Unikernel](https://en.wikipedia.org/wiki/Unikernel)，支持linux应用程序。ruxos基于组件化的kernel框架[ArceOS](https://github.com/rcore-os/arceos)来构建。ArceOS定义了一系列的操作系统不同模块之间的交互接口。ruxos致力于在此框架之上添加实际系统所需要的模块，以及替换和优化内建的模块，用以适配不同的应用场景。与ArceOS一样，ruxos 使用Rust语言进行开发，能够充分利用Rust语言自身的安全特性，方便的构建工具以及快速发展的扩展库。

项目地址: [https://github.com/syswonder/ruxos](https://github.com/syswonder/ruxos) 

邮件列表: [unikernel@syswonder.org](https://maillist.syswonder.org/mailman3/lists/unikernel.syswonder.org/)
