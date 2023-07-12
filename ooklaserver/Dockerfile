FROM ubuntu

MAINTAINER Se7e <eliashenrique.pyc@gmail.com>

WORKDIR /srv

RUN apt-get update && apt-get install -y wget  && apt-get install -y nano

RUN wget http://install.speedtest.net/ooklaserver/ooklaserver.sh
RUN chmod a+x ooklaserver.sh
RUN ./ooklaserver.sh install -f

EXPOSE 8080
EXPOSE 5060

CMD ["./OoklaServer"]
