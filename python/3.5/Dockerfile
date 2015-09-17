FROM        python:3.5
MAINTAINER  duanhongyi <duanhongyi@doopai.com>

RUN apt-get update && apt-get install -y --no-install-recommends \
            binutils \
            gdal-bin \
            libproj-dev \
        && rm -rf /var/lib/apt/lists/*

RUN echo "Etc/UTC" > /etc/timezone
RUN dpkg-reconfigure -f noninteractive tzdata
