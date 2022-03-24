FROM debian:latest
RUN apt update && apt install -y dialog && apt install sudo vim curl apt-utils
ARG USER=al
RUN useradd -m -s /bin/bash $USER \
    && usermod -aG sudo $USER \
    && cp .ssh/  /home/$USER/ -a \
    && chown -R $USER:$USER /home/$USER/.ssh \
    && $USER:$USER | chpasswd
USER $USER
WORKDIR /home/$USER
CMD ["bash"]
