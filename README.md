# 通过JitPack发布Android库使用 Gradle 4.1

tags: jitpack gradle4.01

---

[TOC]

### 1.创建Android项目并添加一个Library库
![images](http://i4.bvimg.com/574168/b45947b5430f5f76.png)

### 2.添加android-maven插件到根目录/build.gradle文件中
![images](http://i4.bvimg.com/574168/5c4a3c24b4a7385d.png)

### 3.在library库的/build.gradle添加maven插件和组设置

![images](http://i4.bvimg.com/574168/6874063a9f5fe02c.png)

### 4.测试，在terminal终端使用gradlew install命令测试
它会将你的库安装在你的本地maven仓库
```
Microsoft Windows [版本 10.0.16299.371]
(c) 2017 Microsoft Corporation。保留所有权利。

E:\rain\demo>gradlew install

BUILD SUCCESSFUL in 9s
24 actionable tasks: 24 executed
E:\rain\demo>

```
这里需要检查 android-maven plugin的版本和Gradle 版本
Gradle version is specified in gradle/wrapper/gradle-wrapper.properties file.
![images](http://i4.bvimg.com/574168/b929f787c3a64d88.png)
Plugin Version 对应 Gradle Version [查看链接](https://github.com/dcendents/android-maven-gradle-plugin#note-on-releases)
![images](http://i4.bvimg.com/574168/51d3390b6b14594e.png)

### 上传项目到github并创建新版本
点击release
![images](http://i2.bvimg.com/574168/115cda66375a6a6a.png)
![images](http://i2.bvimg.com/574168/bc12ff33b4e7fff6.png)

然后打开[JitPack](https://jitpack.io)并查找库
![iamges](http://i2.bvimg.com/574168/10007d4e9c9b4d9d.png)

具体使用方式在该页面自行查看。

