FROM python:3.7-alpine
MAINTAINER  duanhongyi <duanhongyi@doopai.com>

RUN echo "http://dl-cdn.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories

RUN apk add --no-cache --virtual .python-rundeps \
            git \
            geos-dev \
            binutils \
            gdal \
            proj4-dev \
            gcc \
            musl-dev \
            postgresql-dev \
            freetype-dev \
            jpeg-dev \
            libwebp-dev \
            tiff-dev \
            libpng-dev \
            lcms2-dev \
            openjpeg-dev \
            zlib-dev \
    && ln -s /lib/libz.so /usr/lib/ \
    && ln -s /usr/lib/libgdal.so.20 /usr/lib/libgdal.so

RUN pip install pillow \
            psycopg2 \
            gevent \
            gunicorn
