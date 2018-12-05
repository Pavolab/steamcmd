FROM debian:stretch

MAINTAINER Pavolab <https://github.com/Pavolab>

ARG STEAMCMD_URL=https://steamcdn-a.akamaihd.net/client/installer/steamcmd_linux.tar.gz
ARG STEAMCMD_HASH=cfc463be19d2a305412b897b050a3a94c81ddbf6

RUN apt-get update && apt-get install -y \
        lib32gcc1 \
        curl \
        ca-certificates \
        && apt-get -y upgrade \
        && apt-get clean autoclean \
        && apt-get autoremove -y \
        && useradd -m steam

USER steam

RUN mkdir -p /home/steam/steamcmd && cd /home/steam/steamcmd \
    && curl -sqL "${STEAMCMD_URL}" | tar zxvf - \
    && rm -rf /var/lib/{apt,dpkg,cache,log} /tmp/* steamcmd_linux.tar.gz

VOLUME [ "/home/steam/steamcmd" ]