FROM debian:latest

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y dialog apt-utils sudo vim curl

ARG USER=al

RUN useradd -m -s /bin/bash $USER \
    && usermod -aG sudo $USER \
    && echo $USER:$USER | chpasswd

USER $USER

WORKDIR /home/$USER
