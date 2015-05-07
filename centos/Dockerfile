#
# CentOS 6.6
#
FROM centos:6.6
MAINTAINER Takamatsu Makoto <tkmtmkt@gmail.com> (@tkmtmkt_1971)

WORKDIR /root/alminium-dev

RUN yum -y install git which tar && \
    git clone -b tkmtmkt/develop https://github.com/tkmtmkt/alminium.git . && \
    /bin/bash smelt

CMD [ "/bin/bash" ]
