# 矽望开源社区历史

## 背景和动因

矽望syswonder社区于2022年末创建，致力于泛在操作系统的开源发展与建设，关注面向不同应用场景的泛在>操作系统构建及应用技术，推动泛在操作系统在不同领域的落地。

是随着微电子、计算机、人工智能、新一代通信技术
等信息技术的高速发展，人类正在进入一个人机物融合、万物智能互联的泛在计算新时代。
[人机物三元融合新型计算模式](http://old2022.bulletin.cas.cn/publish_article/2022/1/20220107.htm)开始出现，信息设备数量将达万亿级（主要是各种物端设备），新型应用
不断涌现，这些都对现有信息基础设施--包括芯片、操作系统、网络、计算平台等--提出了
新的挑战和需求。

北京大学的研究人员将未来适应人机物三元融合新型计算模式需求的新型态操作系统称为[“泛在操作系统”](http://www.bulletin.cas.cn/thesisDetails#10.16418/j.issn.1000-3045.20211117009)，并认为由于泛在计算场景的领域行业特定性、泛在计算资源的广谱多样性
和极端特异性，泛在操作系统的领域性和专用性将会比较突出，因此有必要面向不同的应用
模式和场景构建不同的泛在操作系统，为此开展了[面向工业物联网场景的泛在操作系统矽>璓](https://xuos.io)的研究工作。

中科院计算所的研究人员从芯片角度，提出面向广阔但多样化和碎片化应用市场场景，不走
通用芯片应用之路，而是探索通过[面向领域的专门芯片进行软硬件贯通优化以获得竞争优>势](http://www.bulletin.cas.cn/thesisDetails#10.16418/j.issn.1000-3045.20211117002)的设想，并认为AIoT 生态发展路径的未来也许是RISC-V/泛在OS(第5代精简指令集和泛>在操作系统)的联盟。

清华大学的研究人员认为，未来新兴应用领域需要特定的新型专用操作系统。如何让开发新
型操作系统像开发应用一样方便高效是一个挑战性问题。为此，他们开展了基于 Rust 语言
开发各种架构/形态的操作系统内核框架和可重用内核组件的工作，探索[操作系统内核组件
化定制化之路](https://github.com/chyyuu/thoughts/blob/main/tangram-oskits.md)，研发[arceos](https://github.com/arceos-org/arceos)。

在这样的背景下，我们-- 来自北大、清华、中科院计算所、上海交大、浙大、西
工大的一些关注系统软件发展的研究人员-- 基于共同的兴趣发起建立了矽望开源
社区，希望针对需要在近场进行实时感知和态势认知的现场计算场景，开展新型操
作系统的探索研究与实验验证。

矽望社区是一个纯粹的爱好者社区，并不属于任何一家单位。我们尝试通过这种方
式，希望与国内外同样对此感兴趣的研究人员单纯就技术本身开展合作，共同探索
有趣的新技术天地。同时，我们希望能探索出一种有效的新型科研合作模式：定位
前沿，技术引领，市场中立，成果共享，合力打造出有产业影响力的技术与项目。


## 和其他社区互相支持

矽望社区成立之初得到[rcore-os社区](https://rcore-os.cn)和[learningOS社区](https://learningos.cn)的大力支持。rcore-os主要探索基于Rust语言的系统软件（
主要是Kernel、Hypervisor、Runtime、Driver等）设计与构造的新思路，learningos主要>培养操作系统人才。三个社区相互支持与帮助，共同推动操作系统的发展。


![](_media/communities.svg)

### rcore-os社区

[rcore-os开源社区](https://github.com/rcore-os/)主要包含了清华大学和国内外开源爱
好者从2018年以来用Rust语言开发操作系统内核和其它相关组件的OS教学和科研探索。主要
包括：

 - [用于教学的rCore-Tutorial v3 kernel](https://github.com/rcore-os/rCore-Tutorial-v3)
 - [基于rCore-Tutorial v3 kernel的OS教材](https://github.com/rcore-os/rCore-Tutorial-Book-v3/)
 - [支持Linux syscall的rCore kernel](https://github.com/rcore-os/rCore)
 - [支持Linux/Zircon syscall的zCore kernel](https://github.com/rcore-os/zCore)
 - [简单的Hypervisor：RVM](https://github.com/rcore-os/RVM)
 - [组件化kernel框架：arceos](https://github.com/rcore-os/arceos)


### learningOS社区

[开源操作系统训练营learningOS](https://github.com/learningOS)作为一个面向OS教育>的开源社区，致力于培养操作系统人才。它将建立一种长期持续发展的操作系统训练营模式
，即各种操作系统相关的学习资源都开源并整理集中在一起，导师/助教和学生/爱好者之间
基于要做的实验或项目不定期/定期的进行交流。学生/爱好者完成了一定程度的学习和训练
后，除了自身得到能力的提升外，还可获得相关证书和就业/学习等机会和相关推荐等，推>动他在未来的进一步发展。目前的主要项目包括：

- [操作系统课程slides](https://github.com/LearningOS/os-lectures)
- [开源操作系统训练营课程](https://github.com/LearningOS/rust-based-os-comp2023)
- [Rust编程训练课程](https://github.com/LearningOS/rustlings)
- [内核实现比赛课程](https://github.com/LearningOS/oscomp-kernel-training)


## 历届技术委员会成员

* 2023 - 2025：陈渝(主任)，曹东刚，陈康，郭耀，李栋，薛栋梁，张羽，赵永望

* 2026 - 2028：张羽（主任），曹东刚，陈渝，陈康，郭耀，李栋，薛栋梁，赵永望


## 历届开源社区委员会成员

* 2026 - 2028：李栋（主任）
