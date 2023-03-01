# 矽望开源项目

## rcore

Rust实现的操作系统内核及基础构件。

邮件列表: [bulletin@syswonder.org](https://maillist.syswonder.org/mailman3/lists/bulletin.syswonder.org/)

## rvisor

Rust实现的Type-1虚拟机监视器（Hypervisor），采用基于基础构件的可重构设计思想，主要提供硬件资源虚拟化、GuestOS镜像安全隔离和原生任务执行的能力，既可以作为裸金属hypervisor使用，也可以作为RTOS内核使用。

邮件列表: [hypervisor@syswonder.org](https://maillist.syswonder.org/mailman3/lists/hypervisor.syswonder.org/)

## Arceos

Arceos是一个模块化的泛在操作系统，为构建单一内核操作系统提供一种新机制。围绕着操作系统的核心功能，Arceos将定义一系列的操作系统不同模块之间的交互接口。在接口的基础上，Arceos将构建对应的操作系统核心模块。模块化的设计使得Arceos不仅仅能够当做一个操作系统核心来运行，每一个模块的实现可以进行替换，适配不同的应用场景。Arceos 使用Rust语言进行开发，能够充分利用Rust语言自身的安全特性，方便的构建工具以及快速发展的扩展库。Arceos在不同场景下将实现出不同的单一内核操作系统[Unikernel](https://en.wikipedia.org/wiki/Unikernel)。

邮件列表: [unikernel@syswonder.org](https://maillist.syswonder.org/mailman3/lists/unikernel.syswonder.org/)
