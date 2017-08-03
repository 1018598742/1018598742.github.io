---
title: virtualbox问题
date: 2017-08-03 
tags:
---

virtualbox 的打不开的问题

<!-- more -->

### virtual box 打不开时可以通过修改注册表

1. regedit

2. 计算机\HKEY_CLASSES_ROOT\CLSID\\{ 00020420-0000-0000-C000-000000000046}\InprocServer32

   计算机\HKEY_CLASSES_ROOT\CLSID\\{ 00020424-0000-0000-C000-000000000046}\InprocServer32

3. 默认值修改为C:\Windows\System32\oleaut32.dll

   ​

{% asset_img vb1.png vb1 %}



{% asset_img vb2.png vb2 %}



{% asset_img vb3.png vb3 %}