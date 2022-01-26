# docker容器配置仓库
## 项目结构
    docker
    ├── mysql                   通用配置文件夹
    │   ├── data                    - MySQL数据库数据持久化存储文件夹
    │   ├── my.cnf                  - mysql配置文件
    │   └── mysql.yml               - MySQL容器配置文件
    ├── nginx                   通用配置文件夹
    │   ├── conf                    - nginx配置文件
    │   ├── conf.d                  - 
    │   ├── html                    - html页面文件夹
    │   ├── logs                    - 日志文件夹
    │   └── nginx.yml               - Nginx容器配置文件    
    ├── redis                   通用配置文件夹
    │   ├── data                    - Redis数据库数据持久化存储文件夹
    │   ├── redis.conf              - redis配置文件
    │   └── mysql.yml               - Redis容器配置文件
    └── README.md                // 项目文档
## 启动
    MySQL

    Redis

    Nginx
