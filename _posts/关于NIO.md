---
layout:     post
title:      "关于Java NIO"
subtitle:  
date:       2017-02-15
author:     "hfj"
header-img: "img/post-bg-ios9-web.jpg"
catalog:    true
tags:
    - Java
    - NIO
---
### Java NIO提供了与标准IO不同的IO工作方式：

* **Channels and Buffers（通道和缓冲区）：**
标准的IO基于字节流和字符流进行操作的，而NIO是基于通道（Channel）和缓冲区（Buffer）进行操作，数据总是从通道读取到缓冲区中，或者从缓冲区写入到通道中。

* **Asynchronous IO（异步IO）：**
Java NIO可以让你异步的使用IO，例如：当线程从通道读取数据到缓冲区时，线程还是可以进行其他事情。当数据被写入到缓冲区时，线程可以继续处理它。从缓冲区写入通道也类似。

* **Selectors（选择器）：**
Java NIO引入了选择器的概念，选择器用于监听多个通道的事件（比如：连接打开，数据到达）。因此，单个的线程可以监听多个数据通道。

> Java NIO contains the concept of "selectors". A selector is an object that can monitor multiple channels for events (like: connection opened, data arrived etc.). Thus, a single thread can monitor multiple channels for data.

| IO             |NIO            |
| ---------------|---------------|
|Stream oriented |Buffer oriented|
|Blocking IO     |Non blocking IO|
|                |Selectors      |
