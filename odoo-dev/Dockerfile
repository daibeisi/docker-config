############################################################
# Dockerfile to build Odoo Development Environment

# Based on odoo:16.0

############################################################
# syntax=docker/dockerfile:1
FROM odoo:16.0

USER root

COPY ./config/sources.list /etc/apt/

ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt-get update -y && \
    apt-get upgrade -y && \
    apt-get install openssh-server sudo -y && \
    systemctl enable ssh

RUN useradd --create-home --no-log-init --shell /bin/bash daibeisi && \
    adduser daibeisi sudo && \
    echo 'daibeisi:newpassword' | chpasswd

# 设置默认执行的命令，docker run 时运行
CMD /etc/init.d/ssh start && bash