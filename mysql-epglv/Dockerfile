FROM mysql:5.7

RUN mkdir -p /tmp/epglv/src
ADD epglv/* /tmp/epglv/
ADD epglv/src/* /tmp/epglv/src/
ADD setup_epglv.sh /tmp/
RUN /tmp/setup_epglv.sh

ENV LANG de_DE.UTF-8  
ENV LANGUAGE de_DE:de  
ENV LC_ALL de_DE.UTF-8

ADD mysqlepgd.cnf /etc/mysql/conf.d/
ADD mysql-first-time.sql /docker-entrypoint-initdb.d/
