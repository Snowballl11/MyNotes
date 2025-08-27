+++
title = 'Ubuntu'
date = 2024-06-23T15:00:49+08:00
draft = false
+++

## 1 软件更新

- 使用 Software Updater 更新
软件更新器是一个图形化的工具, 用于管理系统中的软件更新. 

- 使用命令更新
```
sudo apt update && sudo apt upgrade
```
命令的作用是先更新软件包列表, 然后升级系统上已安装的软件包.

## 2 安装中文输入法

https://www.bilibili.com/video/BV1tY411q7f1/

## 3 允许root用户远程登录

### 3.1修改root用户密码

打开终端, 输入指令:

```
sudo passwd root
```

![img](https://figurebeed.oss-cn-qingdao.aliyuncs.com/img/1064350-20181019172436504-1455601764.png)

### 3.2安装SSH服务

1. 安装ssh

```
sudo apt-get install openssh-server
```

2. 常用命令

```启动ssh服务
sudo /etc/init.d/ssh start
```

```重启ssh服务
sudo /etc/init.d/ssh restart
```

3. 安装完毕后查看状态

```
sudo service ssh status
```

若出现: Active: <font color=00ff00>active (running)</font> , 表示安装成功, 服务已启动.

![img](https://figurebeed.oss-cn-qingdao.aliyuncs.com/img/vm_ssh11.png)

4. 允许root用户远程登录

```
sudo vim /etc/ssh/sshd_config
```
将 PermitRootLogin 的注释去掉, 然后将后面的参数值改为 yes

修改之前:

![img](https://figurebeed.oss-cn-qingdao.aliyuncs.com/img/1064350-20181019175357865-539673795.png)

修改之后:

![img](https://figurebeed.oss-cn-qingdao.aliyuncs.com/img/1064350-20181019175515750-1734350884.png)

5. 然后重启ssh服务:

```
sudo /etc/init.d/ssh restart
```

### 3.3安装 vsftp 服务器

```
sudo apt-get install vsftpd
```

```
sudo vim /etc/vsftpd.conf
```
将 #write_enable=YES 前面的 # 去掉，然后保存

```重启服务
sudo /etc/init.d/vsftpd restart
```

## 4 ffmpeg

```
ffmpeg -i in.mp4 -vn -c:a copy out.m4a
```