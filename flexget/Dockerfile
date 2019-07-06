FROM alpine:latest
LABEL maintainer "Isaac Asensio <isaac.asensio@gmail.com>"

RUN apk add --update \ 
    python3 \
    py-pip

RUN pip install \
    flexget \
    transmissionrpc

RUN mkdir -p /root/.flexget \
    && mkdir -p /tmp/torrents

ENTRYPOINT ["/usr/bin/flexget"]
CMD ["--loglevel", "info", "daemon", "start"]