---
title: javascript对元素类的添加删除等操作
date: 2017-03-06 16:05:48
tags:
categories:
comments: JavaScript基础
---
我们可以通过classList来操作元素的class
classList有五个方法，分别是：
add(),添加一个class（只允许添加一个类名）
remove(),删除一个class
contains(),检查是否包含包含某个class
toggle(),切换class，如果之前有这个class则删除，若无则添加
item(),传入一个数值，返回对应的class名称

```
var div = document.querySelector('div');

var p = document.querySelector('p');

var classList = div.classList;

classList.add('a');

classList.toggle('b');

classList.remove('b');

alert(classList.contains('a'));

alert(classList.item(0));
	

```
[示例](http://runjs.cn/code/n8ojrx1h)