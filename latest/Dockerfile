FROM debian:latest

ARG DEBIAN_FRONTEND=noninteractive

RUN sed -i '/deb\./s/deb\./ftp\.cn\./' /etc/apt/sources.list \
        && apt-get update \
        && apt-get install -y dialog apt-utils sudo vim curl
