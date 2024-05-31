# 矽望开源项目

## 海狸hvisor

![](_media/hvisor-logo.svg)

海狸hvisor是一款Rust实现的Type-1虚拟机监视器（Hypervisor），采用基于separation kernel的设计思想，主要提供最基础的硬件资源虚拟化、资源分区并安全隔离的机制，将硬件资源组织到各个分区（zone0, zoneU, zoneR）中，各个分区在时间和空间上严格隔离，各个分区的系统独立互不干扰运行。分区里部署运行的系统称为应用体appliance，常以轻量虚拟机方式运行。zone0是hvisor专用分区，承担系统管理任务。zoneU一般承担高算力计算任务，应用体可以是unikernel OS，或者Linux OS；承担实时计算任务的zoneR，应用体一般是面向MCU的RTOS甚至裸机应用。通过Type 1 hypervisor的分区隔离，实时RTOS和非实时的Linux或Android虚拟机可以正常运行，满足各自的应用需求。

hvisor的管理功能交由其根zone（zone0）承担，由一组Linux管理工具[hvisor-tool](https://github.com/syswonder/hvisor-tool)实现。

<i class="fa-brands fa-github"></i> 项目地址: [https://github.com/syswonder/hvisor](https://github.com/syswonder/hvisor) 

<i class="fa-solid fa-envelopes-bulk"></i> 邮件列表: [hypervisor@syswonder.org](https://maillist.syswonder.org/mailman3/lists/hypervisor.syswonder.org/)

<i class="fa-solid fa-users-gear"></i> 贡献者:

|姓名|github id|单位|
|----|---------|----|
|贾越凯|[@equation314](https://github.com/equation314)|清华大学(博士生)|
|丁韶峰|[@KarmaD7](https://github.com/KarmaD7)|清华大学(本科生)|
|李柯越|[@likey99](https://github.com/likey99)|中科院计算所(硕士生)|
|汪文韬|[@Miaowulue](https://github.com/Miaowulue)|北京大学(硕士生)|
|陈林锟|[@Enquisitor-201](https://github.com/Inquisitor-201)|哈尔滨工业大学（深圳）（本科生）, 北京大学(硕士生)|
|杨竣轶|[@comet959](https://github.com/comet959)|中科院计算所(硕士生)|
|陈星宇|[@dallasxy](https://github.com/dallasxy)|中科院计算所(硕士生)|
|李国玮|[@kouweilee](https://github.com/kouweilee)|北京航空航天大学(本科生), 北京大学(硕士生)|
|韩喻泷|[@enkerewpo](https://github.com/enkerewpo)|西北工业大学(本科生), 北京大学(博士生)|
|沈铭|[@BoneInscri](https://github.com/BoneInscri)|杭州电子科技大学(本科生), 西北工业大学(硕士生)|
|李韶航|[@sanchezdorso](https://github.com/sanchezdorso)|武汉大学(本科生), 中科院计算所(硕士生)|
|刘景宇|[@liulog](https://github.com/liulog)|华中科技大学(本科生),  中科院计算所(硕士生)|
|徐仲锴|[@ZhongkaiXu](https://github.com/ZhongkaiXu)|中国矿业大学(北京)(本科生)|


## 如意ruxos

![](_media/ruxos-logo.svg)

如意ruxos是一体内核操作系统[Unikernel](https://en.wikipedia.org/wiki/Unikernel)，支持Linux应用程序。ruxos的部分基础构件来自[ArceOS](https://github.com/rcore-os/arceos)，ruxos完善了内核构件框架并补充添加各种模块，用以适配不同的应用场景，特别是对Linux应用的支持。ruxos 使用Rust语言进行开发，能够充分利用Rust语言自身的安全特性，方便的构建工具以及快速发展的扩展库。为便于应用部署，ruxos提供了一个方便易用的应用镜像构建工具[ruxgo](https://github.com/syswonder/ruxgo)。

<i class="fa-brands fa-github"></i> 项目地址: [https://github.com/syswonder/ruxos](https://github.com/syswonder/ruxos) 

<i class="fa-solid fa-envelopes-bulk"></i> 邮件列表: [unikernel@syswonder.org](https://maillist.syswonder.org/mailman3/lists/unikernel.syswonder.org/)

<i class="fa-solid fa-users-gear"></i> 贡献者:

|姓名|github id|单位|
|----|---------|----|
|贾越凯|[@equation314](https://github.com/equation314)|清华大学(博士生)|
|晏巨广|[@coolyjg](https://github.com/coolyjg)|清华大学(硕士生)|
|汪乐平|[@JOHNKRAM](https://github.com/JOHNKRAM)|清华大学(硕士生)|
|袁世平|[@MrRobertYuan](https://github.com/MrRobertYuan)|北京大学(硕士生)|
|张益程|[@zondayc](https://github.com/zondayc)|中国科学技术大学(硕士生)|
|吴政|[@ken4647](https://github.com/ken4647)|北京大学(硕士生)|
|郑元昊|[@Harris-pku](https://github.com/Harris-pku)|北京大学(硕士生)|
|刘昊文|[@lhw2002426](https://github.com/lhw2002426)|北京大学(本科生, 硕士生)|
|杨泽伟|[@BeichenY1](https://github.com/BeichenY1)|北京大学(硕士生)|
|朱若海|[@Miochyann](https://github.com/Miochyann)|北京大学(硕士生)|
|陈正宁|[@thesayol](https://github.com/thesayol)|北京大学(硕士生)|
|熊思民|[@minminm](https://github.com/minminm)|北京大学(硕士生)|
|徐金阳|[@AuYang261](https://github.com/AuYang261)|北京理工大学(本科生), 北京大学(硕士生)|
|周智|[@Sssssaltyfish](https://github.com/Sssssaltyfish)|清华大学(本科生)|

