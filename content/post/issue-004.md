---
title: "每周分享·第4期"
date: 2019-03-10T00:00:00+08:00
lastmod: 2019-03-10T23:59:59+08:00
draft: false
tags: ["Rust","Go","内存分配","编译器","Flutter","MySQL"]
categories: ["技术分享"]
author: "Walker"
toc: false
autoCollapseToc: false
contentCopyright: '<a rel="license" href="https://creativecommons.org/licenses/by-nc-nd/4.0/deed.zh">自由转载-非商用-非衍生-保持署名</a>'
---

感谢阅读 `每周分享` ，我会把每周看过值得分享的内容记录在这里。

<!--more-->

# 文章

#### [图解 Go 内存分配器](https://media.weibo.cn/article?id=2309404347690665261491)

这是之前推过的一篇文章的中译版。文将从内存的基本知识入手，到一般的内存分配器，进而延伸到 Go 内存分配器，对其进行全方位深层次的讲解。

#### [图解 TCMalloc](https://zhuanlan.zhihu.com/p/29216091)

TCMalloc 是 Google 开发的内存分配器，在不少项目中都有使用，例如在 Golang 中就使用了类似的算法进行内存分配。它具有现代化内存分配器的基本特征：对抗内存碎片、在多核处理器能够 scale。

#### [[英文]使用Rust构建类似于Wireshark过滤器那样的执行引擎](https://blog.cloudflare.com/building-fast-interpreters-in-rust/)

![Lex](/img/parse.png)

Cloudflare公司开源的用于解析Wireshark过滤器语法，并将它们编译器为可执行的IR。该库用于该公司提供的防火墙服务规则解析，所以使用Wireshark的过滤器语法作为DSL。

解析语法一般有三种方式：

- 使用状态机、正则等按字符进行解析
- 使用解析器组合器，比如nom或combine这种工具
- 完全自动化的生成器，可以根据提供的语法自动生成一个解析器，比如pest

但是该库并没有用nom或pest，而是选了第一种解析方式。并且在文章里给出了一些提升解析器性能的经验：

他们认为Rust标准库提供的字符串API完全够用。
使用IndexMap替换了HashMap来进一步提升了两倍性能。
使用trait对象动态分发和闭包来避免实现JIT而带来的一些问题。动态分发的执行效率出乎他们的意料。
选择使用Rust语言实现，对于支持WASM提供了巨大的方便。
该库已经用于Cloudflare公司的生产项目。

#### [MySQL 大表优化方案](https://segmentfault.com/a/1190000006158186)

当MySQL单表记录数过大时，增删改查性能都会急剧下降，可以参考其中的步骤来优化

#### [Leaf：美团分布式ID生成服务开源](https://segmentfault.com/a/1190000018436227)

![Leaf：美团分布式ID生成服务开源](/img/leaf.png)

Leaf是美团基础研发平台推出的一个分布式ID生成服务，名字取自德国哲学家、数学家莱布尼茨的一句话：“There are no two identical leaves in the world.”Leaf具备高可靠、低延迟、全局唯一等特点。目前已经广泛应用于美团金融、美团外卖、美团酒旅等多个部门。

#### [百度的春晚战事](https://mp.weixin.qq.com/s?__biz=MzU0NDEwMTc1MA==&mid=2247491861&idx=1&sn=5be51315f84079d798db03bf731ebd17)

无论悲喜，反正每个中国人都为春晚辟出了一块“专属记忆”。而从2015年开始，中国人的春晚记忆里被点上了一颗“红痣”。那就是——总有一家顶尖互联网公司面带羞赧地走上舞台，给十几亿人发红包。2019年，央视春晚红包招标时间很晚，距离除夕只有一个多月的时间。巨头们都觉得凶险异常，百度却高高举手：我来！我来！所有吃瓜群众都侧目，这种“情商低”的状态，还真是百度的风格。。。接下来中哥就告诉你，2019年2月4日除夕晚上，这片土地上究竟发生了什么。

#### [虽难，但产业互联网的量，远大于消费互联网](https://mp.weixin.qq.com/s?__biz=MzIxNTAzNzU0Ng==&mid=2654621349&idx=1&sn=d24401a9c3aa9f84eb08e74f1127b863)

过去几年，在互联网大军的强势竞争下，传统产业似乎遇到了很大的困境。然而，到了2018年，互联网人却纷纷曝出进军传统产业，一场由技术革新带来的变化可能正在颠覆你的认知。产业数字化栏目第一期《小镇：我们已经不一样了 》，我们一起走进小镇感受了那个越来越多企业同台竞逐的产业江湖。今天，我们继续探讨传统产业与互联网如何通过数字化实现平等对话、融合。

#### [2019年，全球十大突破性技术](https://mp.weixin.qq.com/s?__biz=MzIxNTAzNzU0Ng==&mid=2654621275&idx=2&sn=23e2e6440e07cb19293280826bda5533)

自 2001 年起，《麻省理工科技评论》每年都会评选出当年的“十大突破性技术”，这份在全球科技领域举足轻重的榜单曾精准预测了脑机接口、智能手表、癌症基因疗法、深度学习等诸多热门技术的崛起。

# 资源

#### [awesome-compilers](https://github.com/aalhour/awesome-compilers)

编译器、解释器和运行时环境相关领域的学习资料、工具、框架、平台、技术和源代码项目资源大全新版。

#### [【熟肉】Flutter 快速入门](https://www.bilibili.com/video/av38696227/)

Flutter 快速入门（从油管搬运到B站的），帮助开发者快速了解 Flutter，学起 Flutter 基本用法。
由于该教程发布时间较早，期间 Flutter 版本进行了多次更新迭代，所以在一些语法上会存在一些小区别，从个人的实践经验来看，区别并不大

# 工具

#### [Motirx](https://github.com/agalwood/Motrix)

![Motirx](/img/motirx.png)

Motirx 是一款全能的下载工具，支持下载 HTTP、FTP、BT、磁力链、百度网盘等资源。

#### [snapdrop.net](https://snapdrop.net/)

![snapdrop](/img/snapdrop.net.png)

通过浏览器分享本地文件——灵感来自于苹果的 Airdrop

#### 每日一图

![](/img/20190310.jpeg)

一名登山者在喜马拉雅山脉的18,000英尺高的地方收拾营地，背景中耸立的则是世界第八高的马纳斯鲁山。

> 人是沟通的动物。他不仅依赖于食物，也同样依赖于新闻、信息和娱乐。


本文会同步更新到公众号（程序员私塾）中，欢迎订阅。 

![](/img/WechatIMG147.jpeg)