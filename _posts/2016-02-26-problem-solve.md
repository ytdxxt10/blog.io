---
layout: post
title: Problem&Solve
date: 2016-02-25
categories: blog
tags: [iOS积累]
description: Problem&Solve。

---

#problem1&Solve

问题：'XXXX' was compiled with optimization - stepping may behave oddly; variables may not be available

*工程再编译之后被优化了，所以导致但不的时候程序表现异常，变量也都不能访问了，此时如果你进行断点调试，打po 变量是不会输出内容的*

分析：**这是由于编译的时候选择的是release，而release的时候回做出很多优化，导致上述结果**

解决：**点击和模拟器挨着的工程名选择 Edit Scheme 点击左侧的Run，使右侧的Build Configuration 选为Debug模式，点击Close即可**

