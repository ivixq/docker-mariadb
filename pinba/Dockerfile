FROM alpine:edge
MAINTAINER Erik DeLamarter <erik.delamarter@choobs.com>

ENV MARIADB_MAJOR 10.1
ENV MARIADB_VERSION 10.1.17-r0

RUN echo "@testing http://dl-4.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories
RUN apk add --update \
		bash \
		gosu@testing \
		libevent \
		mariadb=$MARIADB_VERSION \
		mariadb-client \
		protobuf \
		pwgen \
		tzdata \
		&& rm -rf /var/cache/apk/*

COPY	Judy-1.0.5.tar.gz /root/
COPY	build-pinba.sh /
RUN	/build-pinba.sh

RUN	mkdir -p /var/run/mysqld && \
	chown mysql:mysql /var/run/mysqld && \
	mkdir -p /etc/mysql/conf.d

COPY my.cnf /etc/mysql/

VOLUME /var/lib/mysql

COPY docker-entrypoint.sh /
RUN mkdir /docker-entrypoint-initdb.d

ENTRYPOINT ["/docker-entrypoint.sh"]

EXPOSE 3306 30002
CMD ["mysqld"]
