FROM nasoym/socat_web_server
MAINTAINER Sinan Goo

ADD crontab.txt /crontab.txt
RUN /usr/bin/crontab /crontab.txt
RUN touch /var/log/cron.log
ADD handlers /handlers

ENTRYPOINT []
CMD crond && ./run.sh -r /handlers/routes -d /handlers/default

