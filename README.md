# learning_log
学习日志 python
使用vscode编辑

1、建立python虚拟隔离环境
    python -m venv ll_env
2、安装Django
    激活虚拟隔离环境后(ll_env\ll_env\Scripts\active)
    安装 pip install Django
3、在Django中创建项目
    依然是在处于活动的虚拟环境下
    django-admin.py startproject learning_log .
4、创建数据库
    python manage.py migrate
    执行runserver
    