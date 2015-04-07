FROM buildpack-deps:jessie
RUN curl -L https://raw.githubusercontent.com/yyuu/pyenv-installer/master/bin/pyenv-installer | bash
COPY docker-entrypoint /
COPY install /tmp/
RUN /docker-entrypoint /tmp/install
ENTRYPOINT ["/docker-entrypoint"]
CMD ["python"]
