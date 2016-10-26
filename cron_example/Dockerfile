FROM alpine
MAINTAINER Sinan Goo

ADD crontab.txt /crontab.txt
RUN /usr/bin/crontab /crontab.txt
RUN touch /var/log/cron.log

# ENTRYPOINT ["/usr/sbin/crond"]
# CMD ["-f"]
# CMD ["crond", "-f", "-d", "8"]
CMD crond && tail -f /var/log/cron.log

