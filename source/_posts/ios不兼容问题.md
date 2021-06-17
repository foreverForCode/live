---
title: ios不兼容问题
tags: ios
date: 2021-06-17 10:55:08
---


##  iso不兼容集合

> 在开发微信小程序时，很多在安卓手机没有问题的样式问题，在IOS中都会有不兼容的细节问题

### 为什么安卓和IOS在微信小程序不兼容

在微信开发者工具和安卓中，浏览器都是使用chrome内核的，但是在IOS中浏览器使用的是safari，chrome和safari内核不一致，chrome由于是一个独立项目，更新很快，在css中功能更强，所以在微信开发者工具和安卓上表现是一致。

### 案例

#### 1 overflow：hidden，border-radius设置对里层样式不生效

解决方法: 在容器组件添加以下样式

```css
.container{
    overflow:hidden;
    border-radius:10px;
    position:relative;
    z-index:1
}
```

