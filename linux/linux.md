[首页](../README.md)
=====
<!-- TOC -->

- [Linux操作Doc](#linux操作doc)
    - [基础操作](#基础操作)
        - [系统配置](#系统配置)
            - [修改主机名](#修改主机名)
        - [初始化系统配置操作](#初始化系统配置操作)
            - [yum的配置](#yum的配置)
    - [文件操作](#文件操作)
        - [修改文件(夹)的权限和所属](#修改文件夹的权限和所属)
    - [进程操作](#进程操作)
    - [网络管理](#网络管理)
        - [查看端口占用](#查看端口占用)
        - [设置DNS解析](#设置dns解析)
        - [设置静态ip](#设置静态ip)

<!-- /TOC -->
# Linux操作Doc
## 基础操作
### 系统配置
#### 修改主机名
### 初始化系统配置操作
#### yum的配置
```
# 修改阿里云源
1.备份原始的源
cd /etc/yum.repos.d
mv CentOS-Base.repo CentOS-Base.repo.bak

2.下载阿里云yum源
wget -O CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo

3.清理缓存
yum clean all

4.重建缓存
yum makecache
```
## 文件操作
### 修改文件(夹)的权限和所属
```
# 权限
chmod -R 777 /xxx

# Tips
r=4，w=2，x=1 
若要rwx属性则4+2+1=7； 
若要rw-属性则4+2=6； 
若要r-x属性则4+1=5。

# 所属
chown root /home/root   // 修改文件(夹)所属用户
chgrp admin /user/soft  // 修改文件(夹)所属用户组
```
## 进程操作
## 网络管理
### 查看端口占用
```
# lsof
lsof -i :80  //查看80端口占用

# netstat
netstat -anp | grep 80 //查看80端口占用
```
### 设置DNS解析
### 设置静态ip
