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
    
    5.1 定义模型
        修改models.py
    5.2 激活模型
        打开setting.py 看到INSTALLED_APPS片段，即告诉Django哪些应用程序安装在项目中
        这是一个数组，在INSTALLED_APPS中添加创建的应用程序learing_logs(之前startapp
        创建的应用程序)。
        需要让Django修改数据库,需要执行makemigrations命令,命令makemigrations让Django
        确定如何修改数据库，使其能够存储与我们定义的新模型相关联的数据，Django创建一个
        0001——initial.py的迁移文件，这个文件将在数据库中为模型Topic创建一个表。
        应用迁移migrate
        
        ![image](https://github.com/yutao-turbo/learning_log/blob/master/image-dev/migrate.png)
        
        每当需要修改“学习笔记”管理的数据时，都采用如下三个步骤：修改models.py;
        对learning_logs调用makemigrations;让Django迁移项目
    5.3 Django管理网站
        创建超级用户
        createsuperuser
        
        ![image](https://github.com/yutao-turbo/learning_log/blob/master/image-dev/createsuperuser.png)

        项管理网站中注册模型
        ![image](https://github.com/yutao-turbo/learning_log/blob/master/image-dev/admin_welcome.png)



