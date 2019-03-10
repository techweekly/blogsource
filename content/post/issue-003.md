---
title: "每周分享·第3期"
date: 2019-03-01T22:58:00+08:00
lastmod: 2019-03-02T00:00:00+08:00
draft: false
tags: ["Rust","Go","数据库","分布式系统","数学","Leetcode","渗透攻击","高并发"]
categories: ["技术分享"]
author: "Walker"
toc: false
autoCollapseToc: false
contentCopyright: '<a rel="license" href="https://creativecommons.org/licenses/by-nc-nd/4.0/deed.zh">自由转载-非商用-非衍生-保持署名</a>'
---

感谢阅读 `每周分享` ，我会把每周看过值得分享的内容记录在这里。

<!--more-->

# 文章

#### [百万 Go TCP 连接的思考: epoll方式减少资源占用](https://colobu.com/2019/02/23/1m-go-tcp-connection/)

虽然 goroutine 不像 thread, 它很轻量,可以在服务器上启动成千上万个。但是对于一百万的连接，这种`goroutine-per-connection` 的模式就至少要启动一百万个 goroutine，这对资源的消耗也是很大，再加上每个 goroutine 分配的 byte buffer，十几个G轻松就交代了。所以文中介绍使用了一种 epoll 的方式处理处理连接。

#### [Rust的生命周期及所有权机制](http://yuequan.org/rust_ownership_lifetime.html)

Rust 是一门不用使用者操心内存分配的系统编程语言，而要保证这点就需要其复杂的生命周期和所有权机制，文章对此进行了简单的梳理，其实这个机制也正是 Rust 学习成本最高的地方。文章提到目前该语言不好的两个地方——编译速度和学习成本，我倒是觉得对于小白来说难的是学习成本，编译速度并不是问题（毕竟一开始也写不了太庞大的工程），对老手来说编译速度可能就要了老命了😂

#### [[英文]Let's Build a Simple Database](https://cstack.github.io/db_tutorial/)

这系列文章不错，教你用C从头开始构建一个sqlite数据库，感兴趣的可以换成Rust来实现。

#### [白话解析分布式系统，小白也能看懂](https://mp.weixin.qq.com/s/VFCG8j5fFQQtt_-jl4jxIA)

说的太基础了，真的是面向小白的，一点都不懂计算机那种，对于分布式系统入门其实更推荐阅读另外一篇 [Distributed systems
for fun and profit](http://book.mixu.net/distsys/single-page.html) （一篇文章扫净分布式系统主流算法）。

#### [面向分布式系统工程师的分布式系统理论（译）](http://blog.xiayf.cn/2014/08/10/Distributed-systems-theory-for-the-distributed-systems-engineer/)

> 一个分布式系统工程师应该知道些什么分布式系统理论？
> 在这种情况下，一知半解(a little theory)并不会是一件多危险的事情。因此我尝试整理一个列表，罗列出作为一个分布式系统工程师的我认为能够直接应用于我日常工作的一些基本概念；或者让分布式系统工程师完全有能力设计一个新系统的“筹码”。

#### [搞不懂分布式事务？看这篇就够了](https://mp.weixin.qq.com/s/VEx36VLW4UfEFo8ZiGs5cg)

从 2PC 、TCC 到 MQ 再到 SAGA ，感觉还是没有太优雅的方案，能不用就别用吧🤔🤔

#### [支撑百万并发的数据库架构如何设计？](https://mp.weixin.qq.com/s/EV2I9Q2_X6SbQGdya-tF_Q)

对于一个支撑日活百万用户的高并系统，他的数据库架构应该如何设计？很多人第一反应就是：分库分表啊！没错，是的😅😅。文章数据库层面的分库分表到底是用来干什么的以及如何应对不同的场景

#### [[英文] 现实中编写可维护的 GO 程序的建议](https://dave.cheney.net/practical-go/presentations/qcon-china.html)

有关编写 Go 代码的最佳实践的建议，这里有一篇[中译版](https://blog.gokit.info/post/go-best-practice/)。

# 资源

#### [沉浸式学习线性代数！这里有一本全交互的线性代数书](http://immersivemath.com/ila/index.html)

今天，我们给大家介绍一本好玩的线性代数书籍。线性代数的书籍那么多，这本却独具特色。准确来讲，量词似乎不能用「本」，因为它需要在网页上阅读，更重要的是，书里的图是可以动的，读者还可以拖动图。这种交互式图看起来很有意思～

![沉浸式学习线性代数](/img/640.gif)

书籍地址：http://immersivemath.com/ila/index.html


#### [Learning Rust With Entirely Too Many Linked Lists](http://cglab.ca/~abeinges/blah/too-many-lists/book/README.html)

刚看过 Rust 基础语法或教程的可以看这个系列练练手，很多坑都会踩到。

#### [Micro8](https://github.com/Micropoor/Micro8)

渗透攻击超十年，由于年龄，身体原因，自己感觉快要退出一线渗透攻击了。遂打算把毕生所学用文字表写出来。因为文章涉及到敏感的攻击行为，所以好多需要打马赛克，或者是本地以demo的形式表现出来。当这个行业做久了，你也终有一天发现原来事物的本质是如此重要。比如内网渗透的本质是信息搜集。当年某大佬把这条经验传递给我，同样，今天变成老家伙的我，也希望把这条经验传递下去。

#### [Nginx Quick Reference](https://github.com/trimstray/nginx-quick-reference)

作者整理的资源和一些线上操作指南，非官方的 Nginx 参考。

#### [LeetCodeAnimation](https://github.com/MisterBooo/LeetCodeAnimation)

![LeetCodeAnimation](/img/LeetCodeAnimation.gif)

用动画的形式呈现解LeetCode题目的思路。另外也可以关注 https://github.com/liuyubobobo/Play-Leetcode

# 工具

#### [Sloth](https://sveinbjorn.org/sloth)

![Sloth](/img/sloth_screenshot1.jpg)

Sloth 是一个 MAC 应用，可以用来查看应用程序打开的文件和端口。

#### [explainshell](https://explainshell.com/)

![explainshell](/img/explainshell.png)

用可视化的方式解释 shell 命令。遇到复杂的 Bash 命令，可以输入到这个网站，查看该命令的解释。

#### [Tools for Frontend developers](http://frontendtools.com/tools)

![frontendtools](/img/frontendtools.png)

适用于前端开发的工具库

#### 每日一图

![](/img/20190302.jpeg)

太阳落在阿根廷圣卡洛斯德巴里洛切的泻湖上。该地区是一个受欢迎的旅游目的地，特别适合那些喜欢滑雪和徒步旅行等户外活动的人

> 大多数人都高估了他们一天能做的事情，但低估了他们一年能做的事情。

本文会同步更新到公众号（程序员私塾）中，欢迎订阅。 

![](/img/WechatIMG147.jpeg)

