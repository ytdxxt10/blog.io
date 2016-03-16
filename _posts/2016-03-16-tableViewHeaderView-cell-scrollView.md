---
layout: post
title: 如何让tableView的每个Section的headerView随tableView一起滚动
date: 2016-03-16
categories: blog
tags: [iOS积累]
description: Problem&Solve。

---

#如何让tableView的每个Section的headerView随tableView一起滚动


正常情况下
![blog1](https://github.com/ytdxxt10/ytdxxt10.github.io/raw/master/blogImage/tableView1.gif)


```
- (void)scrollViewDidScroll:(UIScrollView *)scrollView {
    CGFloat sectionHeaderHeight = 40;
    if (scrollView.contentOffset.y<=sectionHeaderHeight&&scrollView.contentOffset.y>=0) {
        scrollView.contentInset = UIEdgeInsetsMake(-scrollView.contentOffset.y, 0, 0, 0);
    } else if (scrollView.contentOffset.y>=sectionHeaderHeight) {
        scrollView.contentInset = UIEdgeInsetsMake(-sectionHeaderHeight, 0, 0, 0);
    }
}

```
改完后
![blog2](https://github.com/ytdxxt10/ytdxxt10.github.io/raw/master/blogImage/tableView2.gif)

