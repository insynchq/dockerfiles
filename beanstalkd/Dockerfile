FROM buildpack-deps:jessie
RUN mkdir -p /usr/src/beanstalkd
RUN curl https://codeload.github.com/kr/beanstalkd/tar.gz/v1.9 | tar -xzf - -C /usr/src/
RUN cd /usr/src/beanstalkd-1.9 && make install
RUN mkdir -p /var/binlog
VOLUME ['/var/binlog']
EXPOSE 11300
CMD ["beanstalkd", "-b", "/var/binlog"]
