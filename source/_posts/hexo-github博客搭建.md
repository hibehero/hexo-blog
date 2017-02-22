---
title: hexo-github博客搭建
date: 2017-02-22 14:56:34
tags: hexo github
categories: 博客搭建
comments: 
---
## hexo-github搭建博客教程

本文适合有一定node npm github操作基础，但是如果在搭建博客的时候有问题可以在评论区提出，我会一一解答

需要的工具：node git hexo github next主题

1.安装[nodeJs](http://nodejs.cn/)，这边提供链接直接安装官网安装。安装完之后验证你是否有安装可以打开控制台运行命令

```
node -v
```
出现如下界面就说明node安装成功![image](\images\hexo-github\1.png)因为node安装后之后自带npm包管理器所以运行命令

```
npm -v
```
出现如下界面就说明npm安装成功![image](\images\hexo-github\2.png)
2.安装git，[有详细教程这里不具体介绍](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)
3.node，git都安装好之后开始进行我们的主题搭建博客，[hexo官网](https://hexo.io/zh-cn/)，安装官网的步骤先在本地运行，

```
npm install hexo-cli -g
hexo init blog
cd blog
npm install
hexo server
```

4.好，已经可以在本地运行了，先在我们要把它放到github上去，
- 第一步在github上新建一个项目：![image](\images\hexo-github\3.png)，点击new repository，进入create a new repssitory界面
- 这里只要填两个输入框就好，在repository name一栏填hibehero.github.io，这里要注意啦，因为我的github账号是hibehero，但是你要替换成你的github账号的名称***.github.io，descriotion这一栏可以填写对你的博客的描述，比如：我的博客日记，然后点击create repository就可以了![image](\images\hexo-github\4.png)
5.好，现在我们就要来关联远程库，首先在进入hexo博客运行命令
```
hexo g
```
生成本地静态文件，此时你会发现目录中多了个public文件夹![image](\images\hexo-github\5.png)
进入public文件夹，运行命令

```
git init  //初始化git仓库
git add . //添加public文件夹下所有文件
git commit -m "blog" //上传到git仓库
git remote add origin https://github.com/***/****.github.io.git
git push -u origin master
```
里面的***替换成你的账号名
出现如下界面，输入你的gitbug账号名和密码就好
![image](\images\hexo-github\6.png)

[接着就可以访问你的网站了](https://hibehero.github.io/) 还是要把hibehero账号名替换成自己的