#
# Ubuntu 14.04 LTS
#
FROM ubuntu:14.04
MAINTAINER Takamatsu Makoto <tkmtmkt@gmail.com> (@tkmtmkt_1971)

WORKDIR /root/alminium-dev

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && \
    apt-get -y install git && \
    git clone -b tkmtmkt/develop https://github.com/tkmtmkt/alminium.git . && \
    apt-get -y install `grep -v "^#" inst-script/debian/packages.lst` && \
    rm -rf /root/alminium-dev

FROM alminium/ubuntu14.04:base

RUN apt-get update && \
    apt-get -y install git && \
    git clone -b tkmtmkt/develop https://github.com/tkmtmkt/alminium.git .

RUN [ "/bin/bash","smelt" ]

ENV DEBIAN_FRONTEND dialog

CMD [ "/bin/bash" ]
