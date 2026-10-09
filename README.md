# PythonProject3 (Django Web 应用)

这是一个基于 Python 和 Django 框架开发的 Web 应用程序。项目包含基础的用户管理、信息管理以及天气查询等功能模块，前端使用了 Bootstrap 进行页面布局和美化。

## 📌 项目简介

该项目采用经典的 Django MVT（Model-View-Template）架构，目前主要包含一个名为 `app01` 的核心应用。功能涵盖了用户的登录、用户信息的增删改查（CRUD）、常规信息的添加与展示，以及天气数据的展示。

## 🛠 技术栈

*   **后端语言:** Python 3.x
*   **Web 框架:** Django
*   **数据库:** SQLite3 (默认开发数据库)
*   **前端框架/库:** HTML, CSS, JavaScript, Bootstrap 3

## 📂 目录结构说明

```text
pythonproject3/
├── app01/                      # 核心应用目录
│   ├── migrations/             # 数据库迁移文件目录
│   ├── static/                 # 静态资源文件 (CSS, JS, 图片, 第三方插件)
│   │   └── plugins/bootstrap-3 # 引入的 Bootstrap 3 前端框架
│   ├── templates/              # HTML 模板文件
│   │   ├── login.html          # 登录页面
│   │   ├── user_*.html         # 用户管理相关页面
│   │   ├── info_*.html         # 信息管理相关页面
│   │   └── weather.html        # 天气展示页面
│   ├── admin.py                # Django Admin 后台配置
│   ├── apps.py                 # 应用配置
│   ├── models.py               # 数据库模型定义 (ORM)
│   ├── tests.py                # 单元测试
│   └── views.py                # 视图函数 (业务逻辑处理)
├── pythonproject3/             # 项目主配置目录
│   ├── settings.py             # 项目全局设置 (数据库、应用注册、中间件等)
│   ├── urls.py                 # 项目主路由配置
│   ├── asgi.py                 # ASGI 部署配置
│   └── wsgi.py                 # WSGI 部署配置
├── db.sqlite3                  # SQLite 数据库文件
└── manage.py                   # Django 命令行管理工具
