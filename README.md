# webcoreframe

### 一、介绍

本库旨在帮助后端开发人员快速构建一个基于`flask`框架的后端项目。

1. 高效的脚本工具，快速创建原型
    
    ```shell
    # 查看本库支持的脚本链
    webcoreframe --help
    # 快速创建一个后端项目
    webcoreframe create-project
    # 快速创建一个项目的app
    webcoreframe create-app
    # 快速创建一个用户
    webcoreframe create-user
    # 快速收集前端静态文件
    webcoreframe collect-static
    # 快速启动应用
    webcoreframe run
    ```

2. 内部自带电池

    - 内部支持封装orm、redis、log
    - 内部封装插件（定时任务、邮箱、限流、参数编码、参数加密、响应加密）
    - 内部封装中间件（支持认证、系统日志、黑名单、参数编解码、接口过滤、授权、限流、SQL慢日志）
    - 内部封装用户接口，若您需要走自定义用户接口，在配置中添加 CORE_USER_MODEL 配置项目
    - 内部封装系统接口，用于获取系统状态信息、定时任务信息
    - 内部封装后台管理，快速实现后端模型权限的配置、数据的更新
    - 内部封装cli脚本工具，用于快速创建项目

3. 开发进度

    - [80%]封装orm
        - 读写分离
        - 动态分表
    - [80%] 封装redis
    - [90%] 封装log
    - [90%] 封装插件
    - [90%] 封装中间件
    - [90%] 封装用户接口
    - [90%] 封装系统接口
    - [90%] 封装cli脚本
    - [10%] 封装后台管理
        - 后台界面开发
        - 后台接口联调

4. 相关配置

    参考[config.template](./webcoreframe/tpl/config.template)

### 二、CHANGELOG

- v1.3.20240402141838

    ```markdown
    1. 更新授权中间件
    2. 默认开启接口过滤
    3. 移除flask_restful,避免无法命中error_code
    4. 更新系统总览图表-支持拖动查看时间轴
    5. 后台支持动态分表过滤查询
    ```
- v1.2.20240226090040

    ```markdown
    1. 优化前端页面全屏化
    2. 优化webcoreframe的命令行，支持版本检查、服务启动
    3. 支持MySQL主从配置读写分离
    ```

- v1.0.20240123094716

    ```markdown
    1. 优化前端登录页面验证码的刷新
    2. 优化前端数据表页面不分页bug
    3. 优化前端日志页面过滤&定时任务的分页功能
    4. 优化前端定时刷新token
    5. 后端支持类似drf视图集，API编写更加愉快❛‿˂̵✧
    6. 后端token过期时间配置化&单点化
    ```

- v1.0.20240110112852

    ```markdown
    1. 开发webcoreframe核心功能，支持对sqlalchemy、log、中间件的封装；通过cli命令支持应用模板的生成。
    2. 开发webcoreframe后台界面功能，支持对服务器、数据库数据的监控；支持网站接口的拦截等可视化功能。
    ```
