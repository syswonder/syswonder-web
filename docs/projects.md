# 矽望开源项目

## 海狸hvisor

![](_media/hvisor-logo.svg)


hvisor是矽望社区用Rust语言开发的一款轻量Type-1 hypervisor，通过高效虚拟化技术解决现场计算场景不同任务的安全可靠隔离运行问题。hvisor采用little.BIG二元内核架构设计，功能极简，虚拟机性能接近裸机；核心模块进行形式化验证，安全性高；是开源领域首个同时支持ARM aarch64、RISC-V64、LoongArch64和X86\_64四种体系架构的Rust实现的裸机型虚拟机监控器，已适配RK3588、龙芯3A6000等多款异构SoC硬件，支持Linux、Zephyr、RT-Thread等操作系统，适用性强，是[CCF泛在操作系统开放社区](https://ubios.ccf.org.cn)首批支持孵化项目。

<i class="fa-brands fa-github"></i> 项目地址: [https://github.com/syswonder/hvisor](https://github.com/syswonder/hvisor) 

<i class="fa-solid fa-book"></i> 项目文档: [https://hvisor.syswonder.org](https://hvisor.syswonder.org)

<i class="fa-solid fa-envelopes-bulk"></i> 邮件列表: [hypervisor@syswonder.org](https://maillist.syswonder.org/mailman3/lists/hypervisor.syswonder.org/)

<i class="fa-solid fa-users-gear"></i> 贡献者:

|姓名|github id|单位|
|----|---------|----|
|李昕昊|[@li041](https://github.com/li041)|哈尔滨工业大学(本科生)|
|卢安来|[@agicy](https://github.com/agicy)|北京邮电大学(本科生)|
|蔡蕾|[@162210107](https://github.com/162210107)|南京航空航天大学（本科生）|
|陈震雄|[@Crzax](https://github.com/Crzax)|武汉大学（本科生）|
|刘竞暄|[@PKTH-Jx](https://github.com/PKTH-Jx)|清华大学(本科生), 北京大学(博士生)|
|石全|[@Stone749990226](https://github.com/Stone749990226/)|哈尔滨工业大学（深圳）(本科生), 北京大学(硕士生)|
|刘骏|[@LiuJun5817](https://github.com/LiuJun5817/)|浙江大学(博士生)|
|任航麒|[@ForeverYolo](https://github.com/ForeverYolo)|北京航空航天大学(本科生), 北京大学(硕士生)|
|曾俊|[@ZZJJWarth](https://github.com/ZZJJWarth)|华南理工大学(本科生),北京大学(硕士生)|
|刘天弘|[@Solicey](https://github.com/Solicey)|北京大学(本科生, 硕士生)|
|李坤嵘|[@Misaka19986](https://github.com/Misaka19986)|电子科技大学(本科生)|
|侯云龙|[@ohhhHwH](https://github.com/ohhhHwH)|北京大学(硕士生)|
|廖航|[@CarryLiao5959](https://github.com/CarryLiao5959)|北京大学(硕士生)|
|程宏豪|[@CHonghaohao](https://github.com/CHonghaohao)|郑州大学(硕士生)|
|包子旭|[@Baozixu99](https://github.com/Baozixu99)|河南理工大学（本科生）, 西北工业大学(硕士生)|
|陈林锟|[@Enquisitor-201](https://github.com/Inquisitor-201)|哈尔滨工业大学（深圳）（本科生）, 北京大学(硕士生)|
|陈星宇|[@dallasxy](https://github.com/dallasxy)|中科院计算所(硕士生)|
|李国玮|[@kouweilee](https://github.com/kouweilee)|北京航空航天大学(本科生), 北京大学(硕士生)|
|韩喻泷|[@enkerewpo](https://github.com/enkerewpo)|西北工业大学(本科生), 北京大学(博士生)|
|沈铭|[@BoneInscri](https://github.com/BoneInscri)|杭州电子科技大学(本科生), 西北工业大学(硕士生)|
|李韶航|[@sanchezdorso](https://github.com/sanchezdorso)|武汉大学(本科生), 中科院计算所(硕士生)|
|刘景宇|[@liulog](https://github.com/liulog)|华中科技大学(本科生),  中科院计算所(硕士生)|
|徐仲锴|[@ZhongkaiXu](https://github.com/ZhongkaiXu)|中国矿业大学(北京)(本科生), 中科院计算所(硕士生)|
|杨竣轶|[@comet959](https://github.com/comet959)|中科院计算所(博士生)|
|贾越凯|[@equation314](https://github.com/equation314)|清华大学(博士生)|
|丁韶峰|[@KarmaD7](https://github.com/KarmaD7)|清华大学(本科生)|
|李柯越|[@likey99](https://github.com/likey99)|中科院计算所(硕士生)|
|汪文韬|[@Miaowulue](https://github.com/Miaowulue)|北京大学(硕士生)|
|龚天遥|[@FlowerBlackG](https://github.com/FlowerBlackG)|同济大学(本科生), 上海交通大学(硕士生)|
|封宇婷|[@MacixOwl](https://github.com/MacixOwl)|西安交通大学(本科生), 上海交通大学(硕士生)|


## 如意ruxos

![](_media/ruxos-logo.svg)

如意ruxos是一体内核操作系统[Unikernel](https://en.wikipedia.org/wiki/Unikernel)，支持Linux应用程序。ruxos的部分基础构件来自[ArceOS](https://github.com/rcore-os/arceos)，ruxos完善了内核构件框架并补充添加各种模块，用以适配不同的应用场景，特别是对Linux应用的支持。ruxos 使用Rust语言进行开发，能够充分利用Rust语言自身的安全特性，方便的构建工具以及快速发展的扩展库。为便于应用部署，ruxos提供了一个方便易用的应用镜像构建工具[ruxgo](https://github.com/syswonder/ruxgo)。

<i class="fa-brands fa-github"></i> 项目地址: [https://github.com/syswonder/ruxos](https://github.com/syswonder/ruxos) 

<i class="fa-solid fa-book"></i> 项目文档: [https://ruxos.syswonder.org](https://ruxos.syswonder.org)

<i class="fa-solid fa-envelopes-bulk"></i> 邮件列表: [unikernel@syswonder.org](https://maillist.syswonder.org/mailman3/lists/unikernel.syswonder.org/)

<i class="fa-solid fa-users-gear"></i> 贡献者:

|姓名|github id|单位|
|----|---------|----|
|李飞扬|[@HeartLinked](https://github.com/HeartLinked)|浙江大学(本科生), 北京大学(硕士生)|
|石全|[@Stone749990226](https://github.com/Stone749990226/)|哈尔滨工业大学（深圳）(本科生), 北京大学(硕士生)|
|曾俊|[@ZZJJWarth](https://github.com/ZZJJWarth)|华南理工大学(本科生),北京大学(硕士生)|
|吴政|[@ken4647](https://github.com/ken4647)|北京大学(硕士生)|
|郑元昊|[@Harris-pku](https://github.com/Harris-pku)|北京大学(硕士生)|
|刘昊文|[@lhw2002426](https://github.com/lhw2002426)|北京大学(本科生, 硕士生)|
|朱若海|[@Miochyann](https://github.com/Miochyann)|北京大学(硕士生)|
|陈正宁|[@thesayol](https://github.com/thesayol)|北京大学(硕士生)|
|熊思民|[@minminm](https://github.com/minminm)|北京大学(硕士生)|
|徐金阳|[@AuYang261](https://github.com/AuYang261)|北京理工大学(本科生), 北京大学(硕士生)|
|周智|[@Sssssaltyfish](https://github.com/Sssssaltyfish)|清华大学(本科生)|
|贾越凯|[@equation314](https://github.com/equation314)|清华大学(博士生)|
|晏巨广|[@coolyjg](https://github.com/coolyjg)|清华大学(硕士生)|
|汪乐平|[@JOHNKRAM](https://github.com/JOHNKRAM)|清华大学(硕士生)|
|袁世平|[@MrRobertYuan](https://github.com/MrRobertYuan)|北京大学(硕士生)|
|张益程|[@zondayc](https://github.com/zondayc)|中国科学技术大学(硕士生)|
|杨泽伟|[@BeichenY1](https://github.com/BeichenY1)|北京大学(硕士生)|

## 犀灵通 robonix

***犀照世界 灵通万物 为机器筑心 为具身立构***

<img src="_media/robonix-logo.svg" width=400>

犀灵通 robonix 是一款为具身智能设计的新型操作系统。

具身智能是一种基于具身认知理念的人工智能路径，认为[智能无需表征（注：符号编程）](https://people.csail.mit.edu/brooks/papers/representation.pdf)，而是来自“身体”与“环境”的交互，强调“大脑”与“身体”协同，通过“感知–规划–行动“闭环与外部“环境”交互与学习实现通用人工智能。这里的一个关键问题是：具身智能的“大脑”应该如何构造、如何运行，才能支持机器实现上述理念？

近年来基于深度神经网络大/小模型构造具身智能“大脑”的工作，如[视频-语言-动作 VLA(Vision-Language-Action) ](https://doi.org/10.48550/arXiv.2307.15818)大模型，希望能理解世界和预测世界的[世界模型(World Model)](https://doi.org/10.48550/arXiv.1803.10122)，包括LeCun提出的[具身智能大脑实现架构](https://openreview.net/forum?id=BZ5a1r-kVsf)等，基本都是从AI的角度进行探索，关注模型及学习方法本身。我们认为构造具身智能的“大脑”不仅要考虑AI模型本身，还应该关注如何在系统层面对模型的开发、部署、运行和管理等提供支撑，也就是说需要研究适合具身智能特点的操作系统。为此，我们设计犀灵通 Robonix 具身智能操作系统，探索如何从系统层面构造具身智能“大脑”。

Robonix目标是为具身智能大脑提供跨越异构硬件的系统底座，支持具身智能机器人的用户/开发者方便地开发和部署自己的新模型，让自己的机器人能容易地掌握新技能、完成新任务。思路是将AI模型和具身硬件“软硬解耦”，将模型视为程序，希望支持模型“一次训练，任何机器部署运行”，同时针对"感知–理解-规划-行动"过程的数据处理以及环境交互等共性问题，设计 “感知-互联-认知-控制” 具身智能系统服务框架，方便模型和技能的开发和运行。我们期望Robonix能帮助各种机器人容易地构筑智脑，推动具身智能软硬件独立发展生态，让具身智能机器人更好用和易用。


<i class="fa-brands fa-github"></i> 项目地址: [https://github.com/syswonder/robonix](https://github.com/syswonder/robonix) 

<i class="fa-solid fa-book"></i> 项目文档: [https://robonix.syswonder.org](https://robonix.syswonder.org)

<i class="fa-solid fa-envelopes-bulk"></i> 邮件列表: [robotos@syswonder.org](https://maillist.syswonder.org/mailman3/lists/robotos.syswonder.org/)

<i class="fa-solid fa-users-gear"></i> 贡献者:

|姓名|github id|单位|
|----|---------|----|
|张照博|[@HustWolfzzb](https://github.com/HustWolfzzb) |北京大学(博士后)|
|韩喻泷|[@enkerewpo](https://github.com/enkerewpo)|北京大学(博士生)|
|李国玮|[@kouweilee](https://github.com/kouweilee)|北京大学(硕士生)|
|吴政|[@ken4647](https://github.com/ken4647)|北京大学(硕士生)|
|刘昊文|[@lhw2002426](https://github.com/lhw2002426)|北京大学(硕士生)|
|朱若海|[@Miochyann](https://github.com/Miochyann)|北京大学(硕士生)|
|陈正宁|[@thesayol](https://github.com/thesayol)|北京大学(硕士生)|
|熊思民|[@minminm](https://github.com/minminm)|北京大学(硕士生)|
|徐金阳|[@AuYang261](https://github.com/AuYang261)|北京大学(硕士生)|
|侯云龙|[@ohhhHwH](https://github.com/ohhhHwH)|北京大学(硕士生)|
|刘凯乐|[@kaileliu](https://github.com/kaileliu)|杭州电子科技大学（本科生），北京大学(硕士生)|
|陈衍廷|[@Chenyantt](https://github.com/Chenyantt)|南京大学（本科生），北京大学(硕士生)|
|楼金辉|[@laojiahuo2003](https://github.com/laojiahuo2003)|杭州电子科技大学（本科生）|
|赵龙淳|[@1mujue](https://github.com/1mujue)|北京航空航天大学（本科生）|
|蔡蕾|[@162210107](https://github.com/162210107)|南京航空航天大学（本科生）|
|陈震雄|[@Crzax](https://github.com/Crzax)|武汉大学（本科生）|
