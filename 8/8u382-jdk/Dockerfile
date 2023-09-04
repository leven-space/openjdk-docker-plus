FROM eclipse-temurin:8-jdk-jammy

RUN mkdir /usr/local/arthas /usr/local/elastic-apm /usr/local/arms /usr/local/arms/shenzhen/ /usr/local/skywalking
# add telnet vim command
# add arthas
RUN set -eux; \ 
    apt-get update; \
    apt-get install -y --no-install-recommends telnet vim tcpdump netcat htop traceroute net-tools lsof; \
    apt-get install -y jq ;\
    wget -O /usr/local/arthas/arthas-bin.zip "https://github.com/alibaba/arthas/releases/download/arthas-all-3.7.1/arthas-bin.zip";

# set timezone to Shanghai
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo 'Asia/Shanghai' >/etc/timezone


