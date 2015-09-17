FROM        python:3.5
MAINTAINER  duanhongyi <duanhongyi@doopai.com>

RUN apt-get update && apt-get install -y --no-install-recommends \
            language-pack-en
            binutils \
            gdal-bin \
            libproj-dev \
        && rm -rf /var/lib/apt/lists/*

ENV LANGUAGE en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LC_ALL en_US.UTF-8

RUN locale-gen en_US.UTF-8
RUN dpkg-reconfigure locales

RUN echo "Etc/UTC" > /etc/timezone
RUN dpkg-reconfigure -f noninteractive tzdata
