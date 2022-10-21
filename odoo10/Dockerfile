############################################################
# Dockerfile to build Odoo Project

# Based on Ubuntu

############################################################
FROM ubuntu

WORKDIR /odoo
COPY . /odoo/
RUN python3 -m pip install --upgrade pip -i https://mirrors.aliyun.com/pypi/simple/ && \
    pip install -r requirements.txt -i https://mirrors.aliyun.com/pypi/simple/

# 设置默认执行的命令，docker run 时运行
#CMD service odoo start