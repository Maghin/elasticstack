FROM alpine:3.5

MAINTAINER MERHYLSTUDIO

RUN apk add --no-cache curl \
	&& (crontab -l ; echo "0 2 * * * curl -XDELETE elasticsearch:9200/%3Clogstash-%7Bnow%2Fd-15d%7D%3E%2C%3Cmetricbeat-%7Bnow%2Fd-15d%7D%3E > /dev/null 2>&1") | crontab -

CMD ["crond","-f"]
