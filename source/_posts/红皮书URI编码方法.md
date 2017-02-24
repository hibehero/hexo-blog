---
title: 红皮书URI编码方法
date: 2017-02-23 11:24:28
tags: URI编码
categories: JavaScript基础
comments:
---
Global对象的encodeURI()和encodeURIComponent()方法可以对URI进行编码，以便发送给浏览器；
encodeURI()主要用于整个URI，而encodeURIComponent()主要用于对URI中的某一段进行编码。它们的主要区别在于，encodeURI()不会对本身属于URI的特殊字符进行编码，例如冒号，正斜杠，问号和井字号，而encodeURIComponent()则会对它发现的任何非标准字符进行编码。而他们对应的解码是decodeURI()和decodeURIComponent()；

```
var http = 'https://www.google.com.hk/search?q=js+编码解码'

var encodeHttp = encodeURI(http)

//"https://www.google.com.hk/search?q=js+%E7%BC%96%E7%A0%81%E8%A7%A3%E7%A0%81"

var encodeIComponentHttp = encodeURIComponent(http)

//"https%3A%2F%2Fwww.google.com.hk%2Fsearch%3Fq%3Djs%2B%E7%BC%96%E7%A0%81%E8%A7%A3%E7%A0%81"

decodeURI(encodeHttp)

//"https://www.google.com.hk/search?q=js+编码解码"

decodeURIComponent(encodeIComponentHttp)

//"https://www.google.com.hk/search?q=js+编码解码"

```

URI方法encodeURI()，encodeURICoponent(),decodeURI(),decodeURIComponent()已经替代escape()和unescape()方法。因为URI方法能够编码所有Unicode字符，而原来的方法只能正确地编码ASCII字符。