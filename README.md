<a name="readme-top"></a>
<!-- PROJECT SHIELDS -->

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
<!-- [![LinkedIn][linkedin-shield]][linkedin-url] -->

<!-- PROJECT LOGO -->

<!-- 项目LOGO -->
<br />
<div align="center">
  <a href="http://mkdocs.grft.top">
    <img src="https://xiyou-oss.oss-cn-shanghai.aliyuncs.com/mkdocs/logo.png" alt="Logo" width="480" height="270">
  </a>

  <h3 align="center">操作系统</h3>

  <p align="center">
    <br />
    <a href="http://mkdocs.grft.top/操作系统/"><strong>探索文档 »</strong></a>
    <br />
  </p>
</div>

<!-- 目录 -->
<details>
  <summary>目录</summary>
  <ol>
    <li><a href="#关于项目">关于项目</a></li>
    <li><a href="#什么是操作系统">什么是操作系统</a></li>
    <li><a href="#技术目录">技术目录</a></li>
    <li><a href="#贡献">贡献</a></li>
    <li><a href="#许可证">许可证</a></li>
    <li><a href="#联系方式">联系方式</a></li>
    <li><a href="#鸣谢">鸣谢</a></li>
  </ol>
</details>

## 关于项目

整理了一些操作系统相关理论与汇编的资料，以及单片机开发案例，然后进一步衍生鸿蒙系统的手册以及如何开发

入门级手册，详情请详细参考相关资料

公网资料、笔记地址请访问这里 

- 文档地址: [http://mkdocs.grft.top/操作系统/](http://mkdocs.grft.top/操作系统/)

其他相关技术可以访问我的博客，主页地址请访问这里

- 访问入口：[http://mkdocs.grft.top](http://mkdocs.grft.top)

<p align="right">(<a href="#readme-top">回到顶部</a>)</p>

## 什么是操作系统

操作系统（Operating System, OS）是管理计算机硬件与软件资源的程序，同时也是计算机系统的核心和基础。操作系统的主要目的是为用户应用程序和系统服务提供一个便捷、高效的环境，并且管理硬件设备，如 CPU、内存、存储设备、输入输出设备等。操作系统是计算机系统的关键组件，它使得复杂的硬件操作对用户来说更加透明。

### 操作系统的主要功能可以分为以下几个方面

#### 处理器管理（CPU管理）
+ 任务调度：操作系统负责决定哪个程序或进程可以使用CPU以及它们使用CPU的顺序。
+ 进程控制：它创建和终止进程，管理进程的暂停和继续，以及同步与通信。

#### 内存管理
+ 内存分配：操作系统负责管理计算机的物理内存和虚拟内存，以及分配内存空间给各个程序。
+ 内存保护：确保一个程序不会读写到另一个程序的内存空间，保护进程间的数据不受其他进程影响。

#### 文件系统管理
+ 文件操作：操作系统提供文件的创建、删除、读、写等操作。
+ 目录管理：操作系统负责维护文件系统的目录结构和文件在目录中的组织。

#### 设备管理
+ 驱动程序：操作系统通过驱动程序来管理和控制硬件设备。
+ I/O控制：操作系统负责从输入设备读取数据及向输出设备发送数据。

#### 用户界面
+ 命令行界面（CLI）或图形用户界面（GUI）：这些界面允许用户与操作系统进行交互和控制。

#### 安全和访问控制
+ 用户账户管理：操作系统管理用户账户权限，控制用户对文件和程序的访问。
+ 密码保护：提供认证方法以确保只有授权用户才能进入系统。

### 常见的操作系统
操作系统还可以根据需求和设计有特殊的功能，例如网络功能、错误侦测和处理、支持虚拟化等。

操作系统可以分为不同的类型，包括桌面操作系统、服务器操作系统、嵌入式操作系统等。常见的操作系统有 Microsoft Windows、macOS、Linux、UNIX、Android、iOS 等。

<p align="right">(<a href="#readme-top">回到顶部</a>)</p>


## 技术目录

[目录与大纲](index.md)

### 汇编语言

+ [汇编与指令集](汇编语言/汇编与指令集.md)
+ [因特尔64-ia-32架构指令手册](汇编语言/64-ia-32-architectures-software-developer-vol-1-manual.pdf)
+ [arm 架构指令手册](汇编语言/arm指令集及汇编.pdf)


### 操作系统理论

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


### Linux基础

+ [韩顺平Linux教程](Linux基础/韩顺平_2021图解Linux全面升级.pdf)
+ [常用命令汇总](Linux基础/命令汇总.md)
+ 运维笔记
    + [Bash](运维笔记/bash.md)
    + [命令行的艺术](运维笔记/the-art-of-command-line.md)
    + [部署摘录(有点过时 以官网为准)](https://github.com/coregear/linux)
+ 内核开发
    + [Linux 内核与驱动开发](https://github.com/gatieme/LDD-LinuxDeviceDrivers)
    + [单片机开发](https://www.dotcpp.com/course/scm/)


### 鸿蒙系统

+ [官方文档](https://developer.harmonyos.com/cn/docs/documentation/doc-guides-V3/arkts-get-started-0000001504769321-V3)

<p align="right">(<a href="#readme-top">回到顶部</a>)</p>


<!-- 贡献 -->

## 贡献

贡献是使开源社区成为一个如此令人惊叹的地方，以学习、激励和创造。您所做的任何贡献都将非常感谢。

如果您对使这个项目变得更好有建议，请 fork 该仓库并创建 pull request。您也可以打开一个带有“enhancement”标签的问题。不要忘记给这个项目点个星！再次感谢！

<p align="right">(<a href="#readme-top">返回顶部</a>)</p>


<!-- 许可证 -->
## 许可证

根据 MIT 许可证进行分发。更多信息请参见 [LICENSE.txt](LICENSE)。

<p align="right">(<a href="#readme-top">返回顶部</a>)</p>

<!-- 联系方式 -->
## 联系方式

关注我: [小昊子](https://github.com/worst001)

博客地址: [http://mkdocs.grft.top](http://mkdocs.grft.top)

项目链接: [https://github.com/worst001/mkdocs_os](https://github.com/worst001/mkdocs_os)

<p align="right">(<a href="#readme-top">返回顶部</a>)</p>

## 鸣谢

因为仓库与文档的数量比较大，有些借鉴资料忘了在`参考文档`部分提及原作者与原仓库，若有疏漏请告诉，我及时补上。

所有引用的原资料都确认是开源认证，若有侵权请告知。

[https://developer.huawei.com/consumer/cn/](https://developer.huawei.com/consumer/cn/)

[尚硅谷系列教程资料](http://www.atguigu.com/opensource.shtml)

[https://github.com/gatieme/LDD-LinuxDeviceDrivers](https://github.com/gatieme/LDD-LinuxDeviceDrivers)

[https://github.com/coregear/linux](https://github.com/coregear/linux)

[https://openai.com/chatgpt](https://openai.com/chatgpt)

<p align="right">(<a href="#readme-top">返回顶部</a>)</p>

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
