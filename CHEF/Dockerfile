# Below Docker instructions creates a container which can be #used as a node for Chef environment
FROM ubuntu:16.04
RUN apt-get update
RUN apt-get install -y openssh-server
RUN apt-get install -y vim
RUN apt-get install -y net-tools
RUN apt-get install sudo
RUN useradd -m -d /home/dev -s /bin/bash dev
RUN echo "dev:dev" | chpasswd
RUN sed -i '21i dev    ALL=(ALL:ALL) ALL' /etc/sudoers
USER dev
WORKDIR /home/dev
ENTRYPOINT echo dev | sudo -S service ssh start && /bin/bash

