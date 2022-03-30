# docker容器配置仓库
## 项目结构
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
## 启动
    MySQL
        docker-compose -f mysql.yml up -d
    Redis
        docker-compose -f redis.yml up -d
    Nginx
        docker-compose -f nginx.yml up -d
    Posegresql
        docker-compose up -d
    Ubuntu
        docker-compose up -d
