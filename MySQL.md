[TOC]

MySQL 8.0
====

一、安装
---

1、使用CentOS软件包管理器来安装MySQL8.0服务
```base
# dnf install @mysql
```

2、安装完成后，运行以下命令来启动MySQL服务并使它在启动时自动启动
```base
# systemctl enable --now mysqld
```

3、检查MySQL服务器是否正在运行
```base 
# systemctl status mysqld
```

二、初始化配置
---
```base
# mysql_secure_installation
```
根据提示配置数据库参数，密码必须含有大小写、特殊字符、数字等。

三、设置远程访问权限
---
```base 
mysql> use mysql
mysql> show variables like '%skip_networking%';
mysql> SELECT Host, User FROM user;
mysql> CREATE USER '
```
