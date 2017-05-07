---
title: EventBus 使用
date: 2017-05-07 12:06:05
tags:
---

EventBus 应该是一个一观察者模式和广播(还包含构建者模式)开发的各个线程间传递消息的库。

参考 Github 地址：[EventBus](https://github.com/greenrobot/EventBus)

参考 EventBus 网址：[greenrobot](http://greenrobot.org/eventbus/documentation/)

参考学习网址：[Android消息传递之EventBus 3.0使用详解](http://www.cnblogs.com/whoislcj/p/5595714.html)

<!--more-->

# 使用 EventBus

> 添加依赖

在接收消息的类中要注册监听和取消监听

> `EventBus.getDefault().register(this);`



> `EventBus.getDefault().unregister(this);`

注意：要想收到消息，必须已经注册了监听，不然无法收到消息。

### @Subscribe(threadMode = ThreadMode.MAIN)

括号中的内容可以不写，默认 threadMode = ThreadMode.POSTING

- ThreadMode.POSTING : 事件在哪个线程发出就在那个线程接收消息

- ThreadMode.MAIN : 事件不论在哪个线程发出都会在主线程接收消息

- ThreadMode.BACKGROUND : 在子线程接收消息，若在主线程发布，创建子线程接收，若在子线程就在该子线程接收

- ThreadMode.ASYNC : 在子线程接收消息，不论在哪发布均创建子线程接收

### @Subscribe(sticky = true)

通过粘性事件可以实现订阅在发布之后接到消息

注意 : 发送消息时要用

> `EventBus.getDefault().postSticky`