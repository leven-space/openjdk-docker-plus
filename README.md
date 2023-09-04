# openjdk-docker-plus
[![Docker Stars](https://img.shields.io/docker/stars/levenchen/openjdk-docker-plus.svg)](https://hub.docker.com/r/levenchen/openjdk-docker-plus/)
[![Docker Pulls](https://img.shields.io/docker/pulls/levenchen/openjdk-docker-plus.svg)](https://hub.docker.com/r/levenchen/openjdk-docker-plus/)

Expand based on Dokcer's official OpenJdk, and add some common commands and useful components.

## Support Commands

- telnet
- vim
- tcpdump
- netcat 
- htop
- less
- curl
- wget
- traceroute
- jq


## Support Components

| Name | Version | Install Path |
| -------------------- |--------:|--------:|
| `Arthars`       |    3.7.1 | /usr/local/arthas/


## How to Build

```shell
cd taget dir
docker build -t openjdk-docker-plus:{tag}
```