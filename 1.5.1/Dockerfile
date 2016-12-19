FROM ubuntu:16.04
MAINTAINER Toshiaki Baba <toshiaki@netmark.jp>

ENV DEBIAN_FRONTEND noninteractive
ENV TZ Asia/Tokyo

RUN sed -i.bak -e "s%http://us.archive.ubuntu.com/ubuntu/%http://ftp.jaist.ac.jp/pub/Linux/ubuntu/%g" /etc/apt/sources.list
RUN apt-get -y update \
    && apt-get -y install \
        language-pack-ja-base \
        language-pack-ja \
    && apt-get clean

RUN apt-get -y update \
        && apt-get -y install \
            make \
            python-pip \
        && apt-get clean
RUN pip install Sphinx==1.5.1 sphinx-rtd-theme==0.1.9

VOLUME ["/mnt"]
WORKDIR /mnt
