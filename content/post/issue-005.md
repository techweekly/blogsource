---
title: "每周分享·第5期"
date: 2019-03-17T00:00:00+08:00
lastmod: 2019-03-17T23:59:59+08:00
draft: false
tags: ["MySQL","SlimTrie","索引","RocketMQ","微服务"]
categories: ["技术分享"]
author: "Walker"
toc: false
autoCollapseToc: false
contentCopyright: '<a rel="license" href="https://creativecommons.org/licenses/by-nc-nd/4.0/deed.zh">自由转载-非商用-非衍生-保持署名</a>'
---

> 如果没有完成项目，你再忙碌，也无法掩饰没有成效。

<!--more-->

# 文章

#### [深入理解 MySQL ——锁、事务与并发控制](https://mp.weixin.qq.com/s/JFSDqI5yaOc-Znr6Q1ohVA)

本文对 MySQL 数据库中有关锁、事务及并发控制的知识及其原理做了系统化的介绍和总结，希望帮助读者能更加深刻地理解 MySQL 中的锁和事务，从而在业务系统开发过程中可以更好地优化与数据库的交互。

#### [SlimTrie: 单机百亿文件的极致索引-设计篇](https://openacid.github.io/tech/algorithm/slimtrie-design/#)

介绍了一个全新的索引数据结构: SlimTrie 。对索引数据进行了裁剪、压缩和聚合的方法，对索引进行了极大的优化。

#### [SlimTrie: 单机百亿文件的极致索引-实现篇](https://openacid.github.io/tech/algorithm/slimtrie-impl/)

介绍了 SlimTrie 的实现。

#### [蚂蚁金服开源 SOFAJRaft：生产级 Java Raft 算法库](https://mp.weixin.qq.com/s/pmbI_FyOJJyvg008amPutA)

SOFAJRaft 是一个基于 Raft 一致性算法的生产级高性能 Java 实现，支持 MULTI-RAFT-GROUP，适用于高负载低延迟的场景，从百度的 braft 移植而来，做了一些优化和改进。又有新的源码可看了~

#### [RocketMQ源码分析之消息刷盘](https://zhuanlan.zhihu.com/p/58755005)

RocketMQ的两种刷盘策略：
- 一种是类似强一致的，保证消息存储到文件中的同步策略。
- 一种是提交到内存中就算存储成功，在后台异步进行刷盘的异步策略。

#### [面试官问我，Redis分布式锁如何续期？懵了](https://mp.weixin.qq.com/s/y-8W6H9JriUv557Nhudpow)

提前续期 🤣

# 资源

#### [2019年2月份Github上收获最多Star的10个Java项目](https://segmentfault.com/a/1190000018523871)

快来 star 👻👻

#### [The ggplot flipbook – building charts slowly](https://evamaerey.github.io/ggplot_flipbook/ggplot_flipbook_xaringan.html#1)

![ggplot_flipbook.png](/img/ggplot_flipbook.png)

一份教程，说明如何使用 ggplot 构建图表。

#### [Microservice Architecture](http://t.cn/EM2e3rw)

![Microservice Architecture](/img/microservice-architecture.png)

微服务架构相关的电子书

#### [[英文]程序员数学入门](https://jeremykun.com/primers/)

![pimbook](/img/pimbook.jpg)

一位科技博主Jeremy Kun花了4年时间，写成一本书《程序员数学入门》，在科技论坛Hack News引发热议。
这本书精简了大量数学内容，为程序员提供所需的基本数学知识。不是学霸也没关系，能看懂！

# 工具

#### [hexyl](https://github.com/sharkdp/hexyl)

![hexyl](/img/hexyl.png)

一个命令行的文件十六进制查看工具。它能够以不同的颜色，表示不同的字节内容。

#### 每周图片

![20190317](/img/20190317.jpeg)

中国上海，从这个有利位置，你可以看到环绕城市的道路层

感谢阅读。

本文会同步更新到公众号（程序员私塾）中，欢迎订阅。 

![](/img/WechatIMG147.jpeg)


