---
title: Flask笔记（一）
date: 2018-05-24 17:31:05
author: liuxiaowan
tags: [Flask]
---

# 1 配置与惯例

按照惯例，模板和静态文件分别存储在应用 Python 源代码树下的子目录 'templates '和 'static' 里。

# 2 安装

Flask 依赖两个外部库：'Werkzeug' 和 'Jinja2' 。

- Werkzeug 是一个 WSGI（在 Web 应用和多种服务器之间的标准 Python 接口) 工具集。
- Jinja2 负责渲染模板。

## 2.1 virtualenv

- virtualenv 为每个不同项目提供一份 Python 安装。

### 2.1.1 virtualenv安装

- Mac OS X 或 Linux 下

      $ sudo easy_install virtualenv
      # $ sudo pip install virtualenv

- Ubuntu

    $ sudo apt-get install python-virtualenv

### 2.1.2 创建自己的环境

```
$ mkdir myproject
$ cd myproject
$ virtualenv venv
New python executable in venv/bin/python
Installing distribute............done.
```

### 2.1.3 激活相应的环境

- 在 OS X 和 Linux 上

      $ source venv/bin/activate

- Windows上：

      $ venv\scripts\activate

### 2.1.4 激活 virtualenv 中的 Flask

      $ pip install Flask

### 2.1.5 最新版本的 Flask

在一个全新的 virtualenv 中 git checkout 并运行在开发模式下:

```
$ git clone http://github.com/mitsuhiko/flask.git
Initialized empty Git repository in ~/dev/flask/.git/
$ cd flask
$ virtualenv venv --distribute
New python executable in venv/bin/python
Installing distribute............done.
$ . venv/bin/activate
$ python setup.py develop
...
Finished processing dependencies for Flask
```

执行 git pull origin 来升级到最新版本。
