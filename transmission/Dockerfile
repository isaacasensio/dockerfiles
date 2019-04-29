FROM alpine:latest
LABEL maintainer "Isaac Asensio <isaac.asensio@gmail.com>"

RUN apk --no-cache add \
	transmission-daemon \
	&& mkdir -p /transmission/download \
		/transmission/watch \
		/transmission/incomplete \
		/transmission/config \
	&& chmod 1777 /transmission

ENV TRANSMISSION_HOME /transmission/config

EXPOSE 9091

ENTRYPOINT ["/usr/bin/transmission-daemon"]
CMD [ "--foreground", "--config-dir", "/transmission/config" ]