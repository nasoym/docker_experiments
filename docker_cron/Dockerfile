FROM alpine
MAINTAINER Sinan Goo

ADD crontab.txt /crontab.txt
RUN /usr/bin/crontab /crontab.txt

ENTRYPOINT ["/usr/sbin/crond"]
CMD ["-f"]

