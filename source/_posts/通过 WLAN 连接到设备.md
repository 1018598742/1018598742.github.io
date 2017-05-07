---
title: 通过 WLAN	连接到设备
date: 2017-05-07 12:02:19
tags:
---

舍弃数据线，使用 WIFI 进行项目调试。参考网址：[Android 调试桥](https://developer.android.com/studio/command-line/adb.html?hl=zh-cn#devicestatus)

<!--more-->

1. 使用 USB 电缆将设备连接到主计算机。
2. 设置目标设备以侦听端口 5555 上的 TCP/IP 连接。 $ adb tcpip 5555
3. 不用等待，直接断开 USB 电缆连接。
4. 查找 Android 设备的 IP 地址。
5. 通过 IP 地址识别设备来连接。 $ adb connect device_ip_address
6. 确认主计算机已连接至目标设备。 $ adb devices