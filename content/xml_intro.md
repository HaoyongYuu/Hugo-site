---
title: "爬虫入门教程"
date: 2021-12-27
draft: false
---
# **爬虫入门教程**
该教程总共分为4部分内容：
1. 了解网页
2. 节点及节点之间的关系
3. 节点的抓取与选择
4. 用R与Python对网站进行简单的爬取

- [**爬虫入门教程**](#爬虫入门教程)
  - [**1. 了解网页**](#1-了解网页)
    - [**1.1 认识网页结构**](#11-认识网页结构)
      - [**1.1.1 HTML**](#111-html)
      - [**1.1.2 CSS**](#112-css)
      - [**1.1.3 JScript**](#113-jscript)
    - [**1.2 关于爬虫的合法性**](#12-关于爬虫的合法性)
  - [**2. 节点及节点的关系**](#2-节点及节点的关系)
    - [Wow! Cool!](#wow-cool)

## **1. 了解网页** 
### **1.1 认识网页结构**
网页一般由三部分组成，分别是 HTML（超文本标记语言）、CSS（层叠样式表）和 JScript（活动脚本语言）。
#### **1.1.1 HTML**
首先让我们来看一个简单的网页：

这个网页背后的源代码是：
```
<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8">
    <title>爬虫小组的测试页</title>
</head>

<body>

    <h1>欢迎来到爬虫小组的网页！</h1>
    <p>这是一个简单的测试页</p>

    <h2>团队成员与重要日期</h2>
    <p><b>2020年6月10日</b> — 于昊永加入诺华的日子</p>
    <p><b>2020年8月20日</b> — 杨帆加入诺华的日子</p>
    <p><b>2021年6月1日</b> — 王崧人加入诺华的日子</p>
    <p><b>2021年7月1日</b> — 韩梦岳加入诺华的日子</p>
    <p><b>2021年7月1日</b> — 滕书言加入诺华的日子</p>
    <p><b>2021年7月1日</b> — 姚艾文加入诺华的日子</p>

    <h2>更多信息</h2>
    <p>Gitlab: 
        <a href="http://gitlabce.apps.dit-prdocp.novartis.net/YUHAY/web-crawler-do.git">Web Craler DO</a>
    </p>

</body>
</html>
```
HTML 是整个网页的结构，相当于整个网站的框架。带“＜”、“＞”符号的都是属于 HTML 的标签，并且标签都是成对出现的。

常见的标签如下：
```
<html>..</html> 表示标记中间的元素是网页
<body>..</body> 表示用户可见的内容
<div>..</div> 表示框架
<p>..</p> 表示段落
<li>..</li>表示列表
<img>..</img>表示图片
<h1>..</h1>表示标题
<a href="">..</a>表示超链接
```
#### **1.1.2 CSS**
CSS 表示样式，`<style type="text/css">`表示下面引用一个 CSS，在 CSS 中定义了外观。

我们来看一下加入下面的CSS之后，网页会变成什么样子。

```
    <style type="text/css">
    @import url('https://fonts.googleapis.com/css2?family=ZCOOL+KuaiLe&display=swap');
    body {background-image: url('https://www.statnews.com/wp-content/uploads/2018/05/Novartis-1.jpg');
        font-family: 'ZCOOL KuaiLe';}
    h1 {color: blanchedalmond;font-size: 50px;}
    p {color:tomato; font-size: 25px;}
    h2 {color: yellow;font-size: 30px;}
    a {color:turquoise;}
    </style>
```
#### **1.1.3 JScript**
JScript 表示功能。交互的内容和各种特效都在 JScript 中，JScript 描述了网站中的各种功能。

如果用人体来比喻，HTML 是人的骨架，并且定义了人的嘴巴、眼睛、耳朵等要长在哪里。CSS 是人的外观细节，如嘴巴长什么样子，眼睛是双眼皮还是单眼皮，是大眼睛还是小眼睛，皮肤是黑色的还是白色的等。JScript 表示人的技能，例如跳舞、唱歌或者演奏乐器等。

### **1.2 关于爬虫的合法性**
几乎每一个网站都有一个名为 robots.txt 的文档，当然也有部分网站没有设定 robots.txt。对于没有设定 robots.txt 的网站可以通过网络爬虫获取没有口令加密的数据，也就是该网站所有页面数据都可以爬取。如果网站有 robots.txt 文档，就要判断是否有禁止访客获取的数据。

## **2. 节点及节点的关系** 

### Wow! Cool!
|a|b|
|---|---|
askldjlaskjd|asiodiasdaskjd 

i need to highlight ==so funny==

:joy: :christmas_tree:

