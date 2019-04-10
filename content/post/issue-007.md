---
title: "每周分享·第7期"
date: 2019-03-30T00:00:00+08:00
lastmod: 2019-03-30T23:59:59+08:00
draft: false
tags: ["PostgreSQL","Redis","分布式系统","Raft","Android","Python","数据科学"]
categories: ["技术分享"]
author: "Walker"
toc: false
autoCollapseToc: false
contentCopyright: '<a rel="license" href="https://creativecommons.org/licenses/by-nc-nd/4.0/deed.zh">自由转载-非商用-非衍生-保持署名</a>'
---

> 我们这个时代的痛苦在于，那些愚蠢的人都非常自信，那些有想象力和理解能力的人充满了怀疑和犹豫不决。

<!--more-->

# 文章

#### [[英文]Redis streams as a pure data structure](http://antirez.com/news/128)

Redis 5 引入了一种新的数据结构：Stream。不过大部分人可能只想到用于替换 kafka 会用到的场景，作者亲自写文说明除了这类场景外，也可以将 Stream 当做一种特殊的数据结构去改善目前的应用设计。

#### [PgSQL · 原理介绍 · PostgreSQL中的空闲空间管理](http://mysql.taobao.org/monthly/2019/03/06/)

PostgreSQL的MVCC机制中，更新和删除操作并不是对原有的数据空间进行操作，而是通过对元组（tuple）的多版本形式来实现的。而由此引发了过期数据的问题，即当一个版本的元组对所有事物都不可见时，那么它就是过期的，此时它占用的空间是可以被释放的。

上述过期空间的释放工作是交给VACCUM来进行的。在这个过程中，VACCUM会将数据页上的过期元组的空间标记为可用，而当有新的数据插入时，也会优先使用这些可用空间。因此如何将这些可用空间管理起来，并在需要的时候能够高效地分配出去是一个需要解决的问题。

#### [寻找一种易于理解的一致性算法（扩展版）](https://github.com/maemual/raft-zh_cn/blob/master/raft-zh_cn.md)

Raft 算法论文的中文翻译版，学习 raft 必读。Raft 算法本质上也是一种特殊的 Paxos ，但相较于 Paxos 更易于理解，可作为分布式一致性算法入门。

#### [理论基础 · Raft phd 论文中的 pipeline 优化](http://mysql.taobao.org/monthly/2019/03/08/)

因为 Raft 要求日志的有序，不像 paxos 可乱序执行，因此需要优化，改进性能。Leader 与 Follower 之间如果建立多个连接的话，因为日志要求有序，就有点像 TCP 了，同样需要引入失败重试、本地buffer，可能还需要一定的拥塞控制。

#### [阿里巴巴公司根据截图查到泄露信息的具体员工的技术是什么？](https://www.zhihu.com/question/50735753/answer/122593277)

简要介绍频域手段添加数字盲水印的方法，并进一步验证其抗攻击性。在上述实验的基础上，总结躲避数字盲水印的方法。很高端，以后记得用公司电脑取证不要直接截图，用手机拍照，有摩尔纹干涉，安全一些😋

#### [人工智能如何改变基础科学？](https://mp.weixin.qq.com/s/1EZyzNIsbTJoY52dhGcV-A)

对于AI来说，它的一切输入基于人类当前实验与观测设备所输出的精确数据，因此其在简化与优化定律方面有着更强的天赋，也能够发现人类不易察觉的潜在定律。

#### [数据结构与算法——广度和深度优先搜索](https://segmentfault.com/a/1190000018679258)

温故知新。

#### [微保API网关的探索与实践](https://mp.weixin.qq.com/s/OTyOiccWGyeEnv19w7FMiw)

随着微服务架构的日渐推广和普及，以API网关作为微服务统一入口的模式逐渐为人熟知。处在网络边界上的API网关，一方面，可以承担外网服务所需要的通用、非业务类功能，如：鉴权，监控，服务发现/注册，负载均衡等等；另一方面，可以自然地形成对服务和API的运营管理，实现发布，监控，管理，运营的自动化。


#### [Android技术架构演进与未来](https://mp.weixin.qq.com/s/W38aauoCEEUbL8KvUkb_Rw)

![Android技术架构](/img/640.webp)

Android诞生至今已有10余年，这一路走来Android遇到哪些问题？大版本升级朝着什么方向演进？Android的未来如何？

#### [从技术演变的角度看互联网后台架构](https://cloud.tencent.com/developer/article/1404117)

![互联网后台架构](/img/erxuvumu6o.jpeg)

这个ppt的初衷是希望从近十多年来不同时代不同热点下技术栈的变化来看看我们是如何从最早的 `php/asp/jsp<=>mysql` 这样的两层架构，一个阶段一个阶段演变到现在繁复的大数据、机器学习、消息驱动、微服务架构这样的体系，然后在针对其中比较重要的几个方面来给新入门后台开发的同学起个“提纲目录”的作用。

# 资源

#### [Introduction to Theoretical Computer Science](https://introtcs.org/public/)

哈佛大学开源的理论计算科学导论图书

#### [编写和优化Go代码](https://github.com/dgryski/go-perfbook/blob/master/performance-zh.md)

本文档概述了编写高性能Go代码的最佳实践。

虽然有些讨论会提高单个服务的速度（通过缓存等），但设计高性能的分布式系统已经超出了这项工作的范围。在监控和分布式系统设计方面已经有很好的文章，它包含了一套完全不同的研究和设计权衡理论。

#### [人人都能用英语](https://github.com/xiaolai/everyone-can-use-english)

这本书里的文字，全部的意义，只有两个字：“启发”。

有些知识，不仅要了解，还要深入了解。为了深入了解，不仅要学习，还要实践，更要反复试错，在成功中获得激励，在失败中汲取教训，路漫漫其修远，上下求索才可能修成正果。小到开车，大到创业，个中所需要的知识莫不如是。面对这样的知识，我们要了解

- What──它究竟是什么？
- Why──为什么它是那个样子？
- How──要掌握它、应用它，必须得遵循什么样的步骤？

#### [Python Data Science Handbook](https://github.com/jakevdp/PythonDataScienceHandbook)

![PDSH](/img/PDSH-cover.png)

使用 Python 工具进行数据科学研究的教程，现在全书开源了。

#### [Virgilio](https://github.com/clone95/Virgilio)

又一个从零开始入门数据科学的开源图书，还没完结，可以先关注。

# 工具

#### [code-server](https://github.com/codercom/code-server)

![IDE](/img/ide.png)

可以部署到服务端的 VS Code，功能非常完整。

#### [Supernova Studio](https://blog.prototypr.io/sketch-to-flutter-automatically-cf693ea1c892)

![Supernova Studio](/img/1_jBswKSrPX5EkdXsCmRmeSg.png)

一个可以直接将 Sketch 原型设计图转换为 iOS、Android、React、Flutter 代码的工具

#### 每周一图

![20190331](/img/20190331.jpeg)

“法国的白色卡马格马是美丽和优雅的缩影。在这一天如此接近他们是可怕但令人振奋的”

感谢阅读。

本文会同步更新到公众号（程序员私塾）中，欢迎订阅。 

![](/img/WechatIMG147.jpeg)