FROM        ubuntu-debootstrap:14.10
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

RUN apt-get install -y openjdk-8-jdk \
                       maven \
                       ant

RUN apt-get autoremove -qy --purge openjdk-7-jre \
                                   openjdk-7-jre-headless

RUN rm -rf /var/lib/apt/lists/*
