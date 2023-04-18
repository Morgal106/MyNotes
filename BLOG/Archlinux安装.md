---
title : [ Archlinux系统安装及简单配置 ]
tags : [ linux, archlinux, 系统安装 ]
---
## 制作启动盘
### 所需工具
- ArchLinux系统镜像：访问[ArchLinux - Downloads](https://archlinux.org/download/)下载镜像
- U盘
- 刻录工具：下载[Rufus](https://rufus.ie/zh/)刻录工具
### 制作启动盘
1. 插入U盘，确保U盘数据已备份，刻录过程会清空所有数据
2. 打开Rufus刻录工具
3. 选择下载好的镜像，点击刻录

## 系统安装
### BIOS设置
重启进入BIOS设置从U盘启动，并关闭安全启动
### ArchLinux安装
#### 连接网络
使用`iwctl`指令打开无线网连接工具`iwd`，`iwd`常用指令如下

```iwd
help %帮助指令，查看所有指令
device list %查看所有wlan设备
station 设备名 scan %扫描附近wifi
station 设备名 connect WIFI名 %链接扫描到的WIFI，如果加密需要输入密码
quit %退出iwd
```

如果设备列表中显示`power`为`off`，则需要先退出`iwd`，使用`rfkill unblock wifi`命令启动无线网卡

#### 配置分区
使用`fdisk`工具或者`cfdisk`工具
