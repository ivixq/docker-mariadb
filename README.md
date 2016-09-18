# Choobs MariaDB Docker Image #

## Supported tags and respective `Dockerfile` links ##

- [`10.1`, `latest` (10.1/Dockerfile)](https://github.com/choobs/docker-mariadb/blob/master/10.1/Dockerfile)
- [`pinba` (pinba/Dockerfile)](https://github.com/choobs/docker-mariadb/blob/master/pinba/Dockerfile)

[![Docker Stars](https://img.shields.io/docker/stars/choobs/mariadb.svg)](https://hub.docker.com/r/choobs/mariadb/) [![Docker Pulls](https://img.shields.io/docker/pulls/choobs/mariadb.svg)](https://hub.docker.com/r/choobs/mariadb/) [![Build Status](https://travis-ci.org/choobs/docker-mariadb.svg?branch=master)](https://travis-ci.org/choobs/docker-mariadb)

## Information ##

- Follows mariadb's [official image](https://hub.docker.com/r/library/mariadb/) workflow so all ENV variables and init script *should* work.
- The image is based on the [alpine](https://hub.docker.com/_/alpine/) image and comes in about 100MB lighter than the official mariadb image.
- The `pinba` tag provides the [pinba engine plugin](http://pinba.org) for MySQL.
- This image is tested using [Travis CI](https://travis-ci.org) and [PHPUnit](https://phpunit.de/).
- Report any issues in the github [issue tracker](https://github.com/choobs/docker-mariadb/issues/new).
