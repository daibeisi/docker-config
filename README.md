# docker容器配置仓库

## Dockerfile语法

| 命令         | 说明                                                 |
|:-----------|----------------------------------------------------|
| FROM       | 基于哪个镜像来实现                                          |
| MAINTAINER | 镜像的创建者                                             |
| ENV        | 声明环境变量                                             |
| RUN        | 执行的命令                                              |
| ADD        | 添加宿主机文件到容器里，有需要解压的文件会自动解压                          |
| COPY       | 添加宿主机文件到容器里                                        |
| WORKDIR    | 工作目录                                               |
| EXPOSE     | 容器内应用可使用的端口                                        |
| CMD        | 容器启动后所执行的程序，如果执行docker run后面跟启动命令会被覆盖掉             |
| ENTRYPOINT | 与CMD功能相同，但docker run不会覆盖，如果需要覆盖可增加参数-entrypoint来覆盖 |
| VOLUME     | 将宿主机的目录挂载到容器里                                      |

## 项目结构

```text
    docker
    ├── mysql                   
    │   ├── data                    - MySQL数据库数据持久化存储文件夹
    │   ├── my.cnf                  - mysql配置文件
    │   └── mysql.yml               - MySQL容器配置文件
    ├── nginx                   
    │   ├── conf                    - nginx配置文件
    │   ├── conf.d                  - 
    │   ├── html                    - html页面文件夹
    │   ├── logs                    - 日志文件夹
    │   └── nginx.yml               - Nginx容器配置文件    
    ├── postgresql
    │   └── docker-compose.yml      - postgresql容器配置文件    
    ├── redis
    │   ├── data                    - Redis数据库数据持久化存储文件夹
    │   ├── redis.conf              - redis配置文件
    │   └── mysql.yml               - Redis容器配置文件
    └── README.md                // 项目文档
```


## 启动

| 容器名        | 启动命令                                   |
|:-----------|----------------------------------------|
| mysql      | docker-compose -f mysql.yml up -d      |
| redis      | docker-compose -f redis.yml up -d      |
| nginx      | docker-compose -f nginx.yml up -d      |
| postgresql | docker-compose -f postgresql.yml up -d |
| ubuntu     | docker-compose -f ubuntu.yml up -d     |

