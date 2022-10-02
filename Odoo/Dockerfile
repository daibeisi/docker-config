############################################################
# Dockerfile to build Odoo Project

# Based on Ubuntu

############################################################
# syntax=docker/dockerfile:1

# 设置镜像基于ubuntu
FROM ubuntu

# 设置Python解释器不生成字节码pyc文件
#ENV PYTHONDONTWRITEBYTECODE=1

# 不缓冲stdin、stdout和stderr，默认是缓冲的。相当于设置 python 命令行的 -u 选项
#ENV PYTHONUNBUFFERED=1

WORKDIR /odoo
COPY . /odoo/
RUN apt-get update -y && \
    apt-get upgrade -y && \
    apt-get install -y git python3 gcc python3-dev libxml2-dev libxslt1-dev libevent-dev libsasl2-dev libxrender1 \
    libldap2-dev libpq-dev libpng-dev libjpeg-dev xfonts-75dpi xfonts-base wget xz-utils fontconfig libssl3 python3-pip && \
    wget -q "https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-2/wkhtmltox_0.12.6.1-2.jammy_amd64.deb" -O /tmp/wkhtmltopdf.deb && \
    dpkg -i /tmp/wkhtmltopdf.deb && \
    apt-get -fy install && \
    python3 -m pip install --upgrade pip -i https://mirrors.aliyun.com/pypi/simple/ && \
    pip install -r requirements.txt -i https://mirrors.aliyun.com/pypi/simple/

# 设置默认执行的命令，docker run 时运行
#CMD service odoo start