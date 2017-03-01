---
title: getBoundingClientRect()方法的使用
date: 2017-02-24 10:12:00
tags:
categories: JavaScript基础
comments:
---

使用getBoundingClientRect()方法来获取元素左上角相对于视口的位置


```
var button = document.querySelector('button')

var buttonRect = button.getBoundingClientRect();

buttonRect = {
    bottom: -173,
    height: 26,
    left: 1532.40625,
    right: 1602.125,
    top:-199,
    width:,69.71875
}
```

要想通过getBoundingClientRect()来获取元素相对页面可通过获取滚动条的移动距离来叠加

```
var button = document.querySelector('button')

var buttonRect = button.getBoundingClientRect();

var buttonPagePs = buttonRect.left + document.body.scrollLeft
```

