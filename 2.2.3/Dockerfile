FROM ruby:2.2.3
MAINTAINER twingo.b@gmail.com

ENV LANG C.UTF-8

ENV PHANTOMJS_VERSION 1.9.8

RUN apt-get update && \
    apt-get install -y nodejs mysql-client fonts-ipaexfont-gothic --no-install-recommends && \
    apt-get autoremove -y && \
    apt-get clean all

RUN wget -qO /tmp/phantomjs-$PHANTOMJS_VERSION-linux-x86_64.tar.bz2 https://bitbucket.org/ariya/phantomjs/downloads/phantomjs-$PHANTOMJS_VERSION-linux-x86_64.tar.bz2 \
    && cd /tmp \
    && tar jxf phantomjs-$PHANTOMJS_VERSION-linux-x86_64.tar.bz2 \
    && mv phantomjs-$PHANTOMJS_VERSION-linux-x86_64/bin/phantomjs /usr/local/bin/phantomjs \
    && rm -rf phantomjs-$PHANTOMJS_VERSION-linux-x86_64.tar.bz2 phantomjs-$PHANTOMJS_VERSION-linux-x86_64
