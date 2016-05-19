FROM java:openjdk-8-jdk-alpine
MAINTAINER  duanhongyi <duanhongyi@doopai.com>

RUN echo "http://dl-cdn.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories

RUN apk add --no-cache --virtual .java-rundeps  \
            apache-ant \
            maven
