############################################################
# Dockerfile to build Django Development Environment

# Based on Ubuntu

############################################################
# syntax=docker/dockerfile:1

# 设置镜像基于ubuntu
FROM ubuntu

# 设置Python解释器不生成字节码pyc文件
ENV PYTHONDONTWRITEBYTECODE=1

# 相当于设置 python 命令行的 -u 选项
# 不缓冲stdin、stdout和stderr，默认是缓冲的。
ENV PYTHONUNBUFFERED=1

WORKDIR /docker
COPY . /docker/
RUN mv /etc/apt/sources.list /etc/apt/sources.list.bak && \
    ln -s /docker/sources.list /etc/apt/ && \
    apt-get update -y && \
    python -m pip install --upgrade pip -i https://mirrors.aliyun.com/pypi/simple/ && \
    pip install -r requirements.txt -i https://mirrors.aliyun.com/pypi/simple/

# 设置默认执行的命令，docker run 时运行
#CMD conda activate base
