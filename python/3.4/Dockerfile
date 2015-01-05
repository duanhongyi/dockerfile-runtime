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

# base python runtime
RUN apt-get install -y python3 \
                       python3-dev \
                       python3-pip

# geospatial libraries
RUN apt-get install -y binutils \
                       gdal-bin \
                       libproj-dev

# psycopg2
RUN apt-get install -y libpq-dev

# PIL/Pillow
RUN apt-get install -y libtiff5-dev \
                       libjpeg8-dev \
                       zlib1g-dev \
                       libfreetype6-dev \
                       liblcms2-dev \
                       libwebp-dev \
                       tcl8.6-dev \
                       tk8.6-dev \
                       python3-tk

# xml
RUN apt-get install -y libxml2-dev

# delete apt cache
RUN rm -rf /var/lib/apt/lists/*
