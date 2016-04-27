FROM python:2.7-alpine
MAINTAINER  duanhongyi <duanhongyi@doopai.com>

RUN echo "http://dl-cdn.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories

RUN apk add --no-cache --virtual .build-deps  \
            binutils \
            gdal \
            proj4-dev \
    && apk del .build-deps
