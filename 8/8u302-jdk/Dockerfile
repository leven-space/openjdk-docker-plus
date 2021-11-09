FROM openjdk:8u302-jdk

RUN mkdir /usr/local/arthas /usr/local/elastic-apm /usr/local/arms /usr/local/arms/shenzhen/ /usr/local/skywalking
# add telnet vim command
# add arthas
RUN set -eux; \ 
    apt-get update; \
    apt-get install -y --no-install-recommends telnet vim tcpdump netcat htop traceroute net-tools lsof; \
    apt-get install -y jq ;\
    wget -O /usr/local/arthas/arthas-bin.zip "https://github.com/alibaba/arthas/releases/download/arthas-all-3.5.4/arthas-bin.zip";\
    wget -O /usr/local/elastic-apm/elastic-apm-agent.jar "https://repo1.maven.org/maven2/co/elastic/apm/elastic-apm-agent/1.23.0/elastic-apm-agent-1.23.0.jar";

RUN set -eux; \
    wget http://arms-apm-shenzhen.oss-cn-shenzhen.aliyuncs.com/ArmsAgent.zip -O /usr/local/arms/shenzhen/ArmsAgent.zip;\
    wget https://dlcdn.apache.org/skywalking/8.8.1/apache-skywalking-apm-8.8.1.tar.gz -O /usr/local/skywalking/apache-skywalking-apm.tar.gz;


RUN set -eux; \  
unzip /usr/local/arms/shenzhen/ArmsAgent.zip -d /usr/local/arms/shenzhen/;\
    tar -zxvf /usr/local/skywalking/apache-skywalking-apm.tar.gz -C /usr/local/skywalking/

# set timezone to Shanghai
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo 'Asia/Shanghai' >/etc/timezone


