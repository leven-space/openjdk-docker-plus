FROM openjdk:8u302-jdk

RUN mkdir /usr/local/arthas /usr/local/elastic-apm /usr/local/arms
# add telnet vim command
# add arthas
RUN set -eux; \ 
    apt-get update; \
    apt-get install -y --no-install-recommends telnet vim tcpdump netcat htop traceroute ; \
    apt-get install -y jq ;\
    wget -O /usr/local/arthas/arthas-bin.zip "https://github.com/alibaba/arthas/releases/download/arthas-all-3.5.3/arthas-bin.zip";\
    wget -O /usr/local/elastic-apm/elastic-apm-agent.jar "https://repo1.maven.org/maven2/co/elastic/apm/elastic-apm-agent/1.23.0/elastic-apm-agent-1.23.0.jar";\
    wget -O /usr/local/arms/ArmsAgent.zip "http://arms-apm-hangzhou.oss-cn-hangzhou.aliyuncs.com/ArmsAgent.zip" 

# set timezone to Shanghai
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo 'Asia/Shanghai' >/etc/timezone
RUN unzip /usr/local/arms/ArmsAgent.zip -d /usr/local/arms/

