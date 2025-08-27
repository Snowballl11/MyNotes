![001.PNG](.\img\001.png)

## 一. Docker 简介

### Docker 的定义

Docker是一个用于构建 build、运行 run、传送 share 应用程序的平台。

### Docker 的基本原理和概念

我们需要掌握几个重要概念。如果没有理解清楚概念，会加重你的学习难度，导致学习吃力等问题。

这三个概念就是Docker中的镜像、容器和仓库。

![003.PNG](.\img\003.png)

#### 镜像 images

镜像是一个只读的模板，它可以用来创建容器。

#### 容器 containers

容器是Docker的运行实例，它提供了一个独立的可移植的环境，可以在该环境中运行应用程序。

#### Docker仓库 Registry

Docker 仓库是用来存储 Docker 镜像的地方，最流行和常用的仓库就是 Dockerhub。

## 二. Docker 安装

### Docker 的安装流程

根据官网指导安装

### 插入部分：Docker的体系结构

![003.PNG](.\img\003.png)

Docker 是使用 Client-Server 架构模式，Docker Client 和 Docker Daemon 之间，通过 Socket 或者 RESTFul API 进行通信；

Docker Daemon 就是服务端的守护进程，他负责管理 Docker 的各种资源；

Docker Client 负责向 Docker Daemon 发送请求，Docker Daemon 接收到请求之后进行处理，然后将结果返回给 Docker Client；

这里的 Docker Daemon 是一个后台进程，用来接收并处理来自Docker 客户端的请求，然后将结果返回给客户端。所以我们在终端中输入的各种 Docker 命令，实际上都是通过 Docker 客户端发送给 Docker Daemon 的，然后 Docker Daemon 再进行处理，最后将结果返回给客户端，然后就可以在终端中看到执行结果了。

## 常用命令

## 构建镜像

## 运行容器

## Docker Compose  & Kubernetes