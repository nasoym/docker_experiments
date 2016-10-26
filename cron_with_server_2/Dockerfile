FROM nasoym/socat_web_server
MAINTAINER Sinan Goo

RUN apk add --no-cache curl

ADD crontab.txt /crontab.txt
RUN /usr/bin/crontab /crontab.txt
ADD handlers /handlers

RUN touch /var/log/trigger.log

ENTRYPOINT []
CMD crond && ./run.sh -r /handlers -d /handlers/default

