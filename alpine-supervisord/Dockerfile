FROM alpine:3.3
MAINTAINER Andrei Varabyeu <andrei.varabyeu@gmail.com>


RUN apk --no-cache add supervisor

# sample supervisord file is placed here: /etc/supervisord.conf
COPY supervisord-default.conf /etc/supervisord-default.conf
COPY ping.conf /etc/supervisor.d/ping.conf

EXPOSE 9001

ENTRYPOINT ["/usr/bin/supervisord", "--nodaemon", "--configuration", "/etc/supervisord-default.conf"]
