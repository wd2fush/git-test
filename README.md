
pythonproject3/                # Django项目根目录
├── pythonproject3/            # 项目核心配置目录（和项目同名）
│   ├── __init__.py
│   ├── asgi.py                # ASGI异步服务配置文件
│   ├── settings.py            # 项目全局配置：注册app、静态文件、数据库、模板等
│   ├── urls.py                # 项目总路由，分发请求到各个app
│   └── wsgi.py                # WSGI web服务部署配置
├── app01/                     # Django应用app01
│   ├── migrations/            # 数据库迁移文件目录
│   │   ├── 0001_initial.py    # 第一次迁移，生成数据表脚本
│   │   ├── 0002_departme.py   # 第二次迁移，新增/修改表结构脚本
│   │   └── __init__.py
│   ├── static/                # app内静态资源目录（css/js/img/插件）
│   │   ├── css/               # 样式表文件
│   │   ├── img/               # 图片资源
│   │   ├── js/                # javascript脚本
│   │   └── plugins/           # 第三方插件
│   ├── templates/             # app内HTML模板文件夹
│   │   ├── info_add.html      # 信息新增页面
│   │   ├── info_list.html     # 信息列表页面
│   │   ├── login.html         # 登录页面
│   │   ├── tpl.html           # 公共基础模板（一般用于页面继承）
│   │   ├── user_add.html      # 用户新增页面
│   │   ├── user_list.html     # 用户列表页面
│   │   └── weather.html       # 天气页面
│   ├── __init__.py
│   ├── admin.py               # Django后台管理站点配置
│   ├── apps.py                # app应用配置信息
│   ├── models.py              # 数据模型，定义数据库表结构
│   ├── tests.py               # 单元测试文件
│   └── views.py               # 视图函数，接收请求、处理业务逻辑、返回页面
└── db.sqlite3                 # sqlite3数据库文件（Django默认数据库）

文件	       作用
settings.py	项目最重要配置，注册 app01、配置 templates 模板路径、static 静态文件路径、数据库连接
urls.py	项目总路由，把浏览器 url 请求分发到 app01 的路由
wsgi.py	用于线上部署，web 服务器对接 Django
asgi.py	支持异步 web 服务
# 创建迁移文件
python manage.py makemigrations
# 执行迁移，同步到数据库
python manage.py migrate
# 启动开发服务器
python manage.py runserver
# 创建后台管理员账号
python manage.py createsuperuser
