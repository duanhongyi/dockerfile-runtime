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

# openjdk-7-jdk
RUN apt-get install -y openjdk-7-jdk

# maven
RUN apt-get install -y maven

# ant
RUN apt-get install -y ant

RUN rm -rf /var/lib/apt/lists/*
