FROM debian:latest
RUN apt update && apt install -y dialog && apt install -y sudo vim curl apt-utils
ARG USER=al
RUN useradd -m -s /bin/bash $USER \
    && usermod -aG sudo $USER \
    && echo $USER:$USER | chpasswd
USER $USER
WORKDIR /home/$USER
