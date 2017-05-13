---
title: 我的 Android Studio
date: 2017-05-07 16:18:15
tags:
---

重装电脑后，重新下载了 Android Studio 接下来重新配置了

<!--more-->

下载下来第一次打开，字好小，又想去改字体了，不着急，先找一下之前收藏过的配置博客[第一次使用Android Studio时你应该知道的一切配置](http://www.cnblogs.com/smyhvae/p/4390905.html)



奥，我先来查看一下 SDK 和 JDK 配置了吗，点击![AndroidStudio截图1](C:\Users\Administrator\Desktop\AndroidStudio截图1.png)

查看一下，厉害了，Android Studio 包含了 SDK 和 JDK ，正好配置下 Java 环境变量，找到 Java 的存储路径 C:\Program Files\Android\Android Studio\jre

新建 JAVA_HOME

![java环境变量](C:\Users\Administrator\Desktop\java环境变量.png)

添加 %JAVA_HOME%\bin;%JAVA_HOME%\jre\bin

好了，继续我的 Android Studio 有人喜欢修改主题，我还是用原样吧

下面直接改字体 File ---> Settings![AndroidStudio改字体](C:\Users\Administrator\Desktop\AndroidStudio改字体.png)

关闭重新打开直接加载工程
![AndroidStudio修改重启](C:\Users\Administrator\Desktop\AndroidStudio修改重启.png)

设置大小写不敏感

![AndroidStudio设置大小写不敏感](C:\Users\Administrator\Desktop\AndroidStudio设置大小写不敏感.png)

没改几个设置，我觉得原来的设置已经很人性化了，下面更改几个模版，找到我之前保存 github 上的模版

第一个 懒汉式单例

```
#if (${PACKAGE_NAME} != "")package ${PACKAGE_NAME};#end

#if (${IMPORT_BLOCK} != "")${IMPORT_BLOCK}
#end
#parse("File Header.java")

#if (${VISIBILITY} == "PUBLIC")public #end class ${NAME} #if (${SUPERCLASS} != "")extends ${SUPERCLASS} #end #if (${INTERFACES} != "")implements ${INTERFACES} #end {
    private volatile static ${NAME} ourInstance;
    private ${NAME}() {}
    #if (${VISIBILITY} == "PUBLIC")public #end static ${NAME} getInstance() {
        	if(ourInstance == null){
  			synchronized (${NAME}.class) {
  				if(ourInstance == null){
  					ourInstance = new ${NAME}();
  				}
  			}
  		}
        return ourInstance;
    }
}
```

![AndroidStudio新建模版](C:\Users\Administrator\Desktop\AndroidStudio新建模版.png)

要了解可以自定义，通过快捷键快速生成需要的代码， Live Templetes 中系统已经存在了很多默认的模版，可以参考这写自己的。

