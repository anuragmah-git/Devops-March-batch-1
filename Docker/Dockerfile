FROM ubuntu:16.04
MAINTAINER "swapnilmahajan30@gmail.com"

RUN apt-get update && \
    apt-get install -y openssh-server && \
    apt-get install -y nginx


COPY index.html /var/www/html
ENTRYPOINT service nginx start && bash



