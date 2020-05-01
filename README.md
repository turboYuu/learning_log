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
    ![image](https://github.com/yutao-turbo/learning_log/blob/master/image-dev/runserver.png)
    django的成功页面
    ![image](https://github.com/yutao-turbo/learning_log/blob/master/image-dev/django-welcome.png)
    
5、创建应用程序
    django项目由一系列的应用程序组成，
    在激活python隔离环境，切换到manage.py所在目录，执行startapp
    python manage.py startapp learning_logs 命令，让Django建立创建应用程序所需要的
    基础设施，查看项目目录其中新增文件夹learning_logs。其中最重要的文件是models.py、
    admin.py和view.py。使用models.py来定义要在应用程序中管理的数据。

