FROM alpine
MAINTAINER Sinan Goo

ADD crontab.txt /crontab.txt
ADD script.sh /script.sh
ADD entry.sh /entry.sh
RUN chmod 755 /script.sh /entry.sh
RUN /usr/bin/crontab /crontab.txt

CMD ["/entry.sh"]
