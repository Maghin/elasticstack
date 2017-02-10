FROM httpd:2.4-alpine

MAINTAINER Merhylstudio

RUN apk add --no-cache apr-util-ldap

COPY ./conf "$HTTPD_PREFIX/conf"

VOLUME ./conf/certs

EXPOSE "443"
