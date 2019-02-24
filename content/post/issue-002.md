---
title: "技术分享·第2期"
date: 2019-02-23T22:58:00+08:00
lastmod: 2019-02-23T23:00:00+08:00
draft: false
tags: ["Rust","Go","内存模型","Java","MySQL","MVCC","数据结构","红黑树","单词","JSON","算法","Leetcode","面试","概率统计","机器学习"]
categories: ["技术分享"]
author: "Walker"
toc: false
autoCollapseToc: false
contentCopyright: '<a rel="license" href="https://creativecommons.org/licenses/by-nc-nd/4.0/deed.zh">自由转载-非商用-非衍生-保持署名</a>'
---

感谢阅读 ***技术分享***，这里记录我过去一周感觉还不错的内容。

<!--more-->

# 文章

#### [[英文]「系列文章」Rust内存模型介绍](https://speice.io/2019/02/understanding-allocations-in-rust.html)

Rust 是一中没有 GC 但内存安全的系统编程语言，该系列介绍了关于Rust中的内存，包括栈、堆、全局内存分配器、编译器优化等内容。

#### [[英文]图文详解 GO 的内存分配](https://blog.learngoprogramming.com/a-visual-guide-to-golang-memory-allocator-from-ground-up-e132258453ed)

![GO 的内存分配](/img/go_memory.png)

图文详解 GO 的内存分配机制。

#### [[英文]自JDK 8以来所有Java和JVM功能的分类列表](https://advancedweb.hu/2019/02/19/post_java_8/)

JDK 8 可能是最新的大规模在线上使用的版本了，从 8 到 11，JDK 的更新从未停止，文章分门别类总结了从 JDK 8 以来新增的所有功能列表。

#### [6 天面试、斩获 6 家硅谷巨头 Offer，我是如何做到的？](https://www.infoq.cn/article/gkUZZ_qQ6gCuoqpSAcw3)

又一篇荔枝文，不过看来坚持学习、实践、刷题还是应对面试最基本的策略，文章提到的资料也可以参考下（木有中文版哦😜）。

#### [[英文] KMP 子字符串查找算法的 Java 实现](https://www.solutionfactory.in/posts/Knuth-Morris-Pratt-Substring-Search-Algorithm-with-Java-Example)

我们知道在母字符串 S1 （比如 ABCX`ABCDABC`ABCD）寻找子串 S2 （`ABCDABC`Y）的过程中通过跳过那些已经匹配的字符可以节省大量工作，而我们跳过去的那些字符肯定是在匹配母字符串 S1 过程中已经匹配好（但是下一个字符就不匹配）的字符串（比如匹配到 S1 的第 11 位）的后缀，而已经匹配好的字符串既是 S1 的子串，又是 S2 的子串（这里就是 `ABCDABC`），因此跳过的字符数肯定是从 S2 中不断寻找与前缀匹配的后缀，这就是 KMP 算法的本质。如果听不懂没关系，好好看文章🙃🙃🙃。

#### [MySQL · 引擎特性 · InnoDB MVCC 相关实现](http://mysql.taobao.org/monthly/2018/11/04/)

InnoDB支持MVCC来提高系统读写并发性能。InnoDB MVCC的实现基于Undo log，通过回滚段来构建需要的版本记录。通过ReadView来判断哪些版本的数据可见。同时Purge线程是通过ReadView来清理旧版本数据...

#### [相对友好的红黑树教程](http://rkhcy.github.io/2019/02/14/Red_Black_Tree/)

> 红黑树复杂的地方主要在于对其执行增删操作会破坏上面的红黑属性，因此要有相应的机制恢复。这里的恢复机制除了在介绍 AVL Tree 时讲到的旋转，还多了一种重新着色，顾名思义，把红色变成黑色，黑色变成红色即可。

文章只有图文，没有代码。

#### [制作无边无际的虚拟城市——波函数坍缩 (Wave Collapse Function) 的算法](https://mp.weixin.qq.com/s/WIx-yzbvgwSaKrRMIbgY2w)

本篇文章是讲波函数坍缩（Wave Collapse Function）算法。该算法用于生成游戏地图，比如开放世界的无限地图，永远没有尽头。

#### [中国程序员容易发音错误的单词](https://github.com/shimohq/chinese-programmer-wrong-pronunciation)

中国程序员容易发音错误的单词，我以前一直以为 amazon[ə'meizən] 的发音是很正确的，尴尬了，快看看你有多少发音错误的吧。

#### [每秒解析千兆字节的JSON解析器开源](https://mp.weixin.qq.com/s/CUsFecFrgniByF2SvLnYVA)

GitHub 开源了一 JSON 解析器 simdjson，将其与其他常用解析器进行对比实验，结果显示，simdjson 的解析速度达到 2.2GB/s，远远秒杀其他解析器。

# 资源

#### [一份点赞上千的《算法》讲义，来自20年教学经验的UIUC计算机教授](https://zhuanlan.zhihu.com/p/53933538)

一位从1998年就开始讲课的老教授Jeff Erickson，把他20年来在UIUC讲课的内容整理成了一本算法书，名字简单粗暴，就叫《算法》（Algorithms）。

#### [刷 leetcode 需要哪些基础？](https://www.zhihu.com/question/30737325)

金三银四跳槽季啦，如果需要跳去大公司，那么不可避免的要刷点题才行，这个问题下有很多人给出了不错的建议和资料，可参考一下。

#### [9大门类，99个系列课程，几乎所有AI免费课程都在这里啦](https://zhuanlan.zhihu.com/p/56249178)

整体包括深度学习、机器学习基础、机器学习优化、通用机器学习、强化学习、概率图模型、自然语言处理、计算机视觉和新手入门/暑期学校9个部分。

#### [看见统计——看得见的概率统计入门](https://seeing-theory.brown.edu/cn.html)

![看见统计](/img/seeing-theory.gif)

用数据可视化的方式让概率统计更容易理解。适合辅助学习，不要直接拿来当入门教材😥

#### [Vector Logo Zone](https://www.vectorlogo.zone/)

如果想在你的 README 文件中添加漂亮的 LOGO 可以看看，这里有上千种 SVG 图标。

#### [[英]Crypto 101 ](https://www.crypto101.io/)

Crypto 101 是一门关于密码学的免费入门课程，适用于各种水平和阶段的编程人员。

#### [Can't Unsee ——以找茬的形式学习UI设计](https://cantunsee.space/)

![Can't Unsee](/img/cantunsee.space.png)

每次给出两幅 UI 设计的截图并选出有设计问题的那张，很有意思的学习方式。快来挑战吧！


# 工具

#### 在线生成数据库 ER 图——[dbadiagram.io](https://dbdiagram.io) 

![dbadiagram](/img/dbdiagram.io.png)

一个可以在线使用简单的 `DSL` 语言绘制数据库关系图的工具，可自动排版和导出，以后再也不用担心复杂的数据库关系图啦😋


#### 每日一图

![](/img/photo-1549434999-7c0f57709189.jpeg)

>人生值得欣慰之处便是，每一天都有结束的时候。今天亦不例外。

本文会同步更新到公众号（程序员私塾）中，欢迎订阅。 

![](/img/WechatIMG147.jpeg)