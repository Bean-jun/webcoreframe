# webcoreframe

### 一、介绍

本库旨在帮助后端开发人员快速构建一个基于`flask`框架的后端项目。

1. 高效的脚本工具，快速创建原型
    
    ```shell
    # 查看本库支持的脚本链
    python -m webcoreframe --help
    # 快速创建一个后端项目
    python -m webcoreframe create-project
    # 快速创建一个项目的app
    python -m webcoreframe create-app
    # 快速创建一个用户
    python -m webcoreframe create-user
    # 快速收集前端静态文件
    python -m webcoreframe collect-static
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
