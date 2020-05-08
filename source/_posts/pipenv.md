---
title: pipenv
date: 2020-05-08 15:14:32
tags:
- pipenv
categories:
- python
- 工具
- 环境

---

Python项目环境与依赖管理工具

<!-- more -->

### 安装pipenv
> pip3 install pipenv

### 创建虚拟环境
1. 项目目录下执行：pipenv install,生成2个文件Pipfile和Pipfile.lock，为pipenv包的配置文件,代替原来的requirement.txt。
2. 开发克隆下载：根据此Pipfile 运行命令pipenv install --dev生成自己的虚拟环境。
3. Pipfile.lock 文件是通过hash算法将包的名称和版本，及依赖关系生成哈希值，可以保证包的完整性。

### 安装python包
> 安装requests包：pipenv install requests

### 查看安装包及依赖关系
1. pipenv graph
2. 通过--dev指明只安装在开发环境中：pipenv install --dev requests --three

### 兼容requirements.txt 文件
1. 生成requirements.txt文件：pipenv lock -r --dev > requirements.txt
2. 安装requirements.txt 文件中的包：pipenv install -r requirements.txt

### 运行python代码

1. 方法一
> pipenv run python xxx.py

2. 方法二
> 启动虚拟环境的shell环境
> pipenv shell

### 删除虚拟环境
> pipenv --rm

### 常用命令一览
* pipenv --where                 			列出本地工程路径
* pipenv --venv                  	     	 列出虚拟环境路径
* pipenv --py                    			    列出虚拟环境的Python可执行文件
* pipenv install                 			   创建虚拟环境
* pipenv isntall [moduel]        	   安装包
* pipenv install [moduel] --dev    安装包到开发环境
* pipenv uninstall[module]       	 卸载包
* pipenv uninstall --all         		  卸载所有包
* pipenv graph                   			  查看包依赖
* pipenv lock                    			    生成lockfile
* pipenv run python [pyfile]     	运行py文件
* pipenv --rm                    			   删除虚拟环境