FROM ubuntu:latest

MAINTAINER rohitreddy

RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10 \
    && echo 'deb http://downloads-distro.mongodb.org/repo/ubuntu-upstart dist 10gen' > /etc/apt/sources.list.d/mongodb.list \
    && apt-get update \ 
    && apt-get install -y mongodb-org \ 
    && rm -rf /var/lib/apt/lists/* \
    && mkdir -p /data/db

VOLUME ["/data/db"]

WORKDIR /data

EXPOSE 27017

CMD ["mongod"]