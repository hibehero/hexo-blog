---
title: 全平台兼容的XMLHttpRequest对象
date: 2017-03-16 13:23:30
tags:
categories: JavaScript基础
comments:
---
在现代浏览器中创建ajax请求只要通过XMLHttpRequest对象即可，但是为了兼容IE7以下的版本是只能通过ActiveXObject对象来实现，使用ActiveXObject对象来创建时需要指明一个类似"Microsoft.XMLHTTP"只要的ProgID（程序标识符）；下面我们来创建一个函数来兼容XMLHttpRequest对象
```
function getXHR(){
	var xhr = null;
	if(window.XMLHttpRequest){
		xhr = new XMLHttpRequest();
	}else if(window.ActiveXObject){
		try{
			xhr = new ActiveXObject('MSxml2.XMLHTTP')
		}catch(e){
			try{
				xhr = new ActiveXObject('Microsoft.XMLHTTP')
			}catch(e){
				alert("您的浏览器暂不支持Ajax！")
			}
		}
	}
}
```