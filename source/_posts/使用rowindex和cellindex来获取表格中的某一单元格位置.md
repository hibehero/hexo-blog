---
title: 使用rowindex和cellindex来获取表格中的某一单元格位置
date: 2017-03-01 10:12:08
tags:
categories: JavaScript基础
comments:
---
为了获取表格中某一单元格的位置，我们可以通过先获取行，再获取列来确定单元格的位置；


```
var td = document.querySelect('.td');  //获取单元格(.td)

var tr = td.parentNode; //获取父元素tr

var rowIndex = tr.rowIndex;

var cellindex = td.cellIndex;
```


[示例](http://runjs.cn/code/prbqlvbt)