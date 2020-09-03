---
title: black-mac
date: 2020-09-03 16:39:55
categories:
- 黑苹果安装教程
tags:
- mac
- VMware
- 黑苹果
---

Windows系统使用VMware安装MacOS Catalina 10.15系统（黑苹果）的教程，提供MacOS 10.15系统镜像，虚拟机软件VMware Workstation Pro15.5，unlocker3.02和11.5版本package的darwin.iso下载。

<!-- more -->

## 【安装准备】

1 系统镜像：macOS.Catalina.10.15.0.cdr，已经修改来支持在 VMware Workstation Pro 中运行

2 虚拟机软件：VMware Workstation Pro，版本号不低于 15.5，激活方法自行寻找。

3 unlocker：解锁VMware的MacOS支持，版本号不低于 3.0.2

4 darwin.iso：VMware Tools For Mac，用于解决 安装后，MacOS分辨率太小（1024*768像素），版本号不低于11.5 （注意，官方11.5已经不提供下载，您需要从本页面下载darwin.iso，低版本无法在新的MacOS系统中安装）

以上软件我已经放入百度网盘的分享目录，您可以根据需要下载所需的文件。

链接: https://pan.baidu.com/s/1Nlsa1IMhHElmv7TU2RiTrw 提取码: aygh

具全操作过程请看：虚拟机VMware 15安装Mac Os10.14教程  过程都是一样的

首先，安装 VMware Workstation Pro 15.5，如果你的版本是15.0，不要使用官方的在线升级功能，因为你可能会陷入重启，重新安装的循环。只需要下载最新的安装包，会自动覆盖升级，原来的激活信息会保留。其他版本，从重新安装15.5，再重新激活。

## 安装unlocker：

进入unlocker的目录，如果你是从Git上找到的unlocker，建议直接下载源码，不要下载 Releases 版本。进入源码根目录，右键，以管理员权限运行 win-install.cmd，等待命令执行完毕，解锁 VMware Workstation Pro 安装 MacOS的功能。

### 新建虚拟机：

进入 VMware Workstation Pro 15.5，新建虚拟机，选择 macOS.Catalina.10.15.0.cdr，选择Apple MacOS，版本号选择10.15，这里的版本号一定要选择正确，运行虚拟机，如果顺利，就会进入读条。

### 安装MacOS:

安装分为两步骤，第一步，先进入Mac实用工具，选择磁盘工具，抹盘后，注意分区格式，需要选择 MacEXT日志 分区。

第二步，退出磁盘工具，选择重新安装MacOS，点继续，按照提示，一步步安装MacOS即可。

5 安装VMware Tools：
正常情况下，在第2步，安装 unlocker 时，会自动下载 darwin.iso，并复制到 VMware Tools 的根目录，但是由于官方源的失效，需要我们手动安装。先关闭MacOS，编辑虚拟机设置，在CDROM里，挂载 darwin.iso。然后再次启动MacOS，可以在桌面看到 VMware Tools 的盘符，双击，安装 VMware Tools 后即可。

{% asset_img 1.png VMware安装MacOS Catalina 10.15教程，附darwin.iso下载 %}

注意，这里要选择信任（先点击左下角的图标解锁），允许 系统 安装 VMware Tools。

安装成功后，会自动重启电脑，你就可以看到熟悉的MacOS系统，赶紧全屏，体验一下新系统操作的感觉吧！

【安装效果】

这是在 VMware Workstation Pro 15.5 运行 MacOS Catalina 10.15 的截图：

{% asset_img 2.jpg VMware安装MacOS Catalina 10.15教程，附darwin.iso下载 %}

{% asset_img 3.jpg VMware安装MacOS Catalina 10.15教程，附darwin.iso下载 %}

