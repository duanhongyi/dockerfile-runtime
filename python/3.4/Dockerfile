FROM        ubuntu-debootstrap:14.04
MAINTAINER  duanhongyi <duanhongyi@doopai.com>

RUN sed -i 's/archive.ubuntu.com/mirrors.aliyun.com/g' /etc/apt/sources.list
RUN apt-get update

RUN apt-get install -qy language-pack-en
ENV LANGUAGE en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LC_ALL en_US.UTF-8

RUN locale-gen en_US.UTF-8
RUN dpkg-reconfigure locales

RUN echo "Etc/UTC" > /etc/timezone
RUN dpkg-reconfigure -f noninteractive tzdata

RUN apt-get install -y python3 \
                       python3-pip \
                       binutils \
                       gdal-bin

RUN apt-get install -y python3-dev \
                       libxml2-dev \
                       libpq-dev \
                       libtiff5-dev \
                       libjpeg8-dev \
                       zlib1g-dev \
                       libfreetype6-dev \
                       liblcms2-dev \
                       libwebp-dev \
                       tcl8.6-dev \
                       tk8.6-dev \
                       python3-tk \
                       libproj-dev

RUN rm -rf /var/lib/apt/lists/*
