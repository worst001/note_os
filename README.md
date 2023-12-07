# 操作系统

整理了一些操作系统相关理论与汇编的资料，以及单片机开发案例，然后进一步衍生鸿蒙系统的手册以及如何开发

入门级手册，详情请详细参考相关资料

公网资料、笔记地址请访问这里 


<!-- PROJECT SHIELDS -->

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
<!-- [![LinkedIn][linkedin-shield]][linkedin-url] -->

<!-- PROJECT LOGO -->

--------------------

## 基本介绍

操作系统（Operating System, OS）是管理计算机硬件与软件资源的程序，同时也是计算机系统的核心和基础。操作系统的主要目的是为用户应用程序和系统服务提供一个便捷、高效的环境，并且管理硬件设备，如 CPU、内存、存储设备、输入输出设备等。操作系统是计算机系统的关键组件，它使得复杂的硬件操作对用户来说更加透明。

## 操作系统的主要功能可以分为以下几个方面

### 处理器管理（CPU管理）
+ 任务调度：操作系统负责决定哪个程序或进程可以使用CPU以及它们使用CPU的顺序。
+ 进程控制：它创建和终止进程，管理进程的暂停和继续，以及同步与通信。

### 内存管理
+ 内存分配：操作系统负责管理计算机的物理内存和虚拟内存，以及分配内存空间给各个程序。
+ 内存保护：确保一个程序不会读写到另一个程序的内存空间，保护进程间的数据不受其他进程影响。

### 文件系统管理
+ 文件操作：操作系统提供文件的创建、删除、读、写等操作。
+ 目录管理：操作系统负责维护文件系统的目录结构和文件在目录中的组织。

### 设备管理
+ 驱动程序：操作系统通过驱动程序来管理和控制硬件设备。
+ I/O控制：操作系统负责从输入设备读取数据及向输出设备发送数据。

### 用户界面
+ 命令行界面（CLI）或图形用户界面（GUI）：这些界面允许用户与操作系统进行交互和控制。

### 安全和访问控制
+ 用户账户管理：操作系统管理用户账户权限，控制用户对文件和程序的访问。
+ 密码保护：提供认证方法以确保只有授权用户才能进入系统。

## 常见的操作系统
操作系统还可以根据需求和设计有特殊的功能，例如网络功能、错误侦测和处理、支持虚拟化等。

操作系统可以分为不同的类型，包括桌面操作系统、服务器操作系统、嵌入式操作系统等。常见的操作系统有 Microsoft Windows、macOS、Linux、UNIX、Android、iOS 等。


--------------------

## 目录

[目录与大纲](index.md)

## 汇编语言

+ [汇编与指令集](汇编语言/汇编与指令集.md)
+ [因特尔64-ia-32架构指令手册](汇编语言/64-ia-32-architectures-software-developer-vol-1-manual.pdf)
+ [arm 架构指令手册](汇编语言/arm指令集及汇编.pdf)


## 操作系统理论

+ [计算机操作系统（一）——概览](理论知识/计算机操作系统（一）——概览.md)
+ [计算机操作系统（二）——中断](理论知识/计算机操作系统（二）——中断.md)
+ [计算机操作系统（三）——进程](理论知识/计算机操作系统（三）——进程.md)
+ [计算机操作系统（四）——处理器](理论知识/计算机操作系统（四）——处理器.md)
+ [计算机操作系统（五）——存储管理](理论知识/计算机操作系统（五）——存储管理.md)
+ [计算机操作系统（六）——文件系统](理论知识/计算机操作系统（六）——文件系统.md)
+ [计算机操作系统（七）——IO存储管理](理论知识/计算机操作系统（七）——IO存储管理.md)
+ [计算机操作系统（八）——并发程序设计](理论知识/计算机操作系统（八）——并发程序设计.md)
+ [计算机操作系统（九）——其他](理论知识/计算机操作系统（九）——其他.md)
+ [计算机操作系统(第3版)课后习题答案](理论知识/计算机操作系统(第3版)课后习题答案.md)


## Linux基础

+ [韩顺平Linux教程](Linux基础/韩顺平_2021图解Linux全面升级.pdf)
+ [常用命令汇总](Linux基础/命令汇总.md)
+ 运维笔记
    + [Bash](运维笔记/bash.md)
    + [命令行的艺术](运维笔记/the-art-of-command-line.md)
    + [部署摘录(有点过时 以官网为准)](https://github.com/coregear/linux)
+ 内核开发
    + [Linux 内核与驱动开发](https://github.com/gatieme/LDD-LinuxDeviceDrivers)
    + [单片机开发](https://www.dotcpp.com/course/scm/)


## 鸿蒙系统

+ [官方文档](https://developer.harmonyos.com/cn/docs/documentation/doc-guides-V3/arkts-get-started-0000001504769321-V3)


-------------------

## 贡献者

请阅读**CONTRIBUTING.md** 查阅为该项目做出贡献的开发者。

#### 如何参与开源项目

贡献使开源社区成为一个学习、激励和创造的绝佳场所。你所作的任何贡献都是**非常感谢**的。


1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## 版本控制

该项目使用Git进行版本管理。您可以在repository参看当前可用版本。

<!-- ## 作者 -->
<!--  -->
<!-- [小昊子](https://github.com/worst001) -->
<!--  -->
<!-- 制做不易，如果有帮到你就请作者喝杯咖啡吧! -->
<!--  -->
<!-- ![支付宝加微信](https://xiyou-oss.oss-cn-shanghai.aliyuncs.com/%E5%85%AC%E4%BC%97%E5%8F%B7%E4%B8%8E%E6%94%AF%E4%BB%98/%E6%94%AF%E4%BB%98%E5%AE%9D%E5%8A%A0%E5%BE%AE%E4%BF%A1.jpg) -->
<!--  -->
<!-- 作者无聊时做的测试游戏，完全免费哦！ -->
<!--  -->
<!-- ![公众号](https://xiyou-oss.oss-cn-shanghai.aliyuncs.com/%E5%85%AC%E4%BC%97%E5%8F%B7%E4%B8%8E%E6%94%AF%E4%BB%98/%E5%85%AC%E4%BC%97%E5%8F%B7%E5%B0%8F.jpg) -->

## 参考资料

[https://developer.huawei.com/consumer/cn/](https://developer.huawei.com/consumer/cn/)

[尚硅谷系列教程资料](http://www.atguigu.com/opensource.shtml)

<!-- links -->
[your-project-path]:shaojintian/Best_README_template
[contributors-shield]: https://img.shields.io/github/contributors/worst001/mkdocs_os.svg?style=flat-square
[contributors-url]: https://github.com/worst001/mkdocs_os/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/worst001/mkdocs_os.svg?style=flat-square
[forks-url]: https://github.com/worst001/mkdocs_os/network/members
[stars-shield]: https://img.shields.io/github/stars/worst001/mkdocs_os.svg?style=flat-square
[stars-url]: https://github.com/worst001/mkdocs_os/stargazers
[issues-shield]: https://img.shields.io/github/issues/worst001/mkdocs_os.svg?style=flat-square
[issues-url]: https://img.shields.io/github/issues/worst001/mkdocs_os.svg
[license-shield]: https://img.shields.io/github/license/worst001/mkdocs_os.svg?style=flat-square
[license-url]: https://github.com/worst001/mkdocs_os/blob/main/LICENSE.txt
<!-- [linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555 -->
<!-- [linkedin-url]: https://linkedin.com/in/shaojintian -->
