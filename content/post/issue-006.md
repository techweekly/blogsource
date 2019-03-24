---
title: "每周分享·第6期"
date: 2019-03-24T00:00:00+08:00
lastmod: 2019-03-24T23:59:59+08:00
draft: false
tags: ["性能","CPU","密码学","Rust","数据库","算法"]
categories: ["技术分享"]
author: "Walker"
toc: false
autoCollapseToc: false
contentCopyright: '<a rel="license" href="https://creativecommons.org/licenses/by-nc-nd/4.0/deed.zh">自由转载-非商用-非衍生-保持署名</a>'
---

> 对于学习而言是没有捷径的，任何的工具和方法最终还是需要你亲自去执行。

<!--more-->

# 文章

#### [性能瓶颈诊断--CPU篇(一）](https://bryantchang.github.io/2019/03/09/cpu-profile/)

![](/img/linux_perf_tools_full.png)

系列文章，作者总结的一系列性能相关的文章，涉及CPU、内存、IO，这是性能诊断套路之CPU篇，常见CPU指标以及相应原理。还没有完结，赶紧关注吧！

#### [一文读懂椭圆曲线加密学](https://mp.weixin.qq.com/s/Mxk_YR5Ba_MOy3on85twmA)

本文是关于椭圆曲线加密的非常基础的介绍。内容虽然基础，但对于椭圆曲线加密的门外汉来说，简单易懂，适合于初学者。真得好简单，比 RSA 还简单 😁~

#### [服务发现-注册中心概述](https://juejin.im/post/5c3d708f5188252410607847)

本文通过研究一些开源服务注册发现框架，总结其设计要点。

#### [使用Rust编写操作系统（二）：最小化内核](https://zhuanlan.zhihu.com/p/56433770)

系列文章，使用 Rust 语言编写简单的操作系统，麻雀虽小，五脏俱全，这是第二篇，主要说明了如何配置 Rust 编译环境以及通过 BIOS 引导一个简单的内核映像（打印字符到 VGA 缓冲区）。

#### [[英文]Understanding The Memcached Source Code - Event Driven I](https://holmeshe.me/understanding-memcached-source-code-VII/)

系列文章，Memcached 的源码分析，重点介绍了 SLAB 分配器、LRU 算法、事件驱动模型和一致性哈希。Memcached 的线程模型是典型的 dispatcher-worker 模式。

#### [[英文]Pathfinding Demystified (Part I): Generic Search Algorithm](http://www.gabrielgambetta.com/generic-search.html)

路径搜索在游戏开发中很常见，但很多程序员对此知之甚少，这个系列文章主要就是为了介绍常用的路径搜索与 A* 算法。

#### [大 O 表示法](http://rkhcy.github.io/2019/03/06/bigO/)

![](/img/bigo_12.png)

大 O 符号是用来描述算法复杂度的，不同的复杂度到底有怎样的直观表示呢？

#### [高性能JavaScript读书笔记](https://juejin.im/post/5c9458d8f265da6115608d78)

点到为止，可作为 checkpoint。

#### [[英文]Toy Markets](https://blog.ycombinator.com/toy-markets/)

现在做大了的超级大公司一开始都是针对极小的市场，做的东西看起来也像玩具一样。一个创业者如果做的东西像玩具一样，怎么说服投资人给你钱？

大部分投资人其实也没经历过任何“玩具”时期的创业公司，能进入他们视野的公司普遍都已经看起来像真的公司了。可以尝试从两个方面来解释“玩具”如何做大：1，可以扩展到类似的市场（一开始卖书，以后可以卖dvd、买玩具、卖电器等）；2，用户的行为会有变化（用桌面电脑上网 -> 用手机上网）。

# 资源

#### [How Database works](https://architecture-database.blogspot.com/)

一个关于数据库内部架构的网站，需要翻墙。

#### [.NET 平台架构](https://github.com/sidristij/dotnetbook)

![donetbook](/img/BookCover-ch.png)

可以说，本书是对.NET CLR原理的全面描述，一定程度上包含了.NET Framework，主旨是为了让读者从一个不同且不寻常的角度来看待它的内部结构。还没完结， 可以先关注一下。

#### [Top 50 Dynamic Programming Practice Problems](https://medium.com/@codingfreak/top-50-dynamic-programming-practice-problems-4208fed71aa3)

50 个可用 `动态规划` 解决的问题


#### [Java-Crypto-Utils](https://github.com/tunjos/java-crypto-utils)

Java 的加/解密、编码、哈希工具库

#### [SOFA 公开文章](https://www.yuque.com/huarou/gd4szw)

![](/img/SOFA.PNG)

蚂蚁金服开源技术文章合集


#### 每周一图

![20190324](/img/20190324.jpeg)

雪中的大峡谷。“这些下面的岩石层的图案和形状被揭示出这种复杂的美丽，只有在被雪地亲吻时才能看到。真是美好的一天”。

感谢阅读。

本文会同步更新到公众号（程序员私塾）中，欢迎订阅。 

![](/img/WechatIMG147.jpeg)
