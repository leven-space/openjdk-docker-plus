FROM openjdk:8u292-jdk

RUN mkdir /usr/local/arthas
# add telnet vim command
# add arthas
RUN set -eux; \ 
    apt-get update; \
    apt-get install -y --no-install-recommends telnet vim; \
    wget -O /usr/local/arthas/arthas-bin.zip "https://github.com/alibaba/arthas/releases/download/arthas-all-3.5.0/arthas-bin.zip"
# set timezone to Shanghai
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo 'Asia/Shanghai' >/etc/timezone

