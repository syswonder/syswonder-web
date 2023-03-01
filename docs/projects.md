# 矽望开源项目

## rcore-os

rcore-os开源社区主要包含了清华大学和国内外开源爱好者从2018年以来用Rust语言开发操作系统内核和其它相关组件的OS教学和科研探索。主要包括：

- [用于教学的rCore-Tutorial v3 kernel](https://github.com/rcore-os/rCore-Tutorial-v3)
- [基于rCore-Tutorial v3 kernel的OS教材](https://github.com/rcore-os/rCore-Tutorial-Book-v3/)
- [支持Linux syscall的rCore kernel](https://github.com/rcore-os/rCore)
- [支持Linux/Zircon syscall的zCore kernel](https://github.com/rcore-os/zCore)
- [简单的Hypervisor：RVM](https://github.com/rcore-os/RVM)
- [组件化kernel框架：arceos](https://github.com/rcore-os/arceos)

以及各种奇怪的OS、hypervisor、runtime、driver、与OS无关并可用于组合出不同OS的组件等（驱动，文件系统、网络协议栈等）。

邮件列表: [bulletin@syswonder.org](https://maillist.syswonder.org/mailman3/lists/bulletin.syswonder.org/)

## rvisor

Rust实现的Type-1虚拟机监视器（Hypervisor），采用基于基础构件的可重构设计思想，主要提供硬件资源虚拟化、GuestOS镜像安全隔离和原生任务执行的能力，既可以作为裸金属hypervisor使用，也可以作为RTOS内核使用。

邮件列表: [hypervisor@syswonder.org](https://maillist.syswonder.org/mailman3/lists/hypervisor.syswonder.org/)

## rlibos

Rust实现的库形态泛在操作系统实例, 设计思想来自[Unikernel](https://en.wikipedia.org/wiki/Unikernel)。

邮件列表: [unikernel@syswonder.org](https://maillist.syswonder.org/mailman3/lists/unikernel.syswonder.org/)
