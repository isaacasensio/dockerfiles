FROM alpine:latest
LABEL maintainer "Isaac Asensio <isaac.asensio@gmail.com>"

RUN apk add --update --no-cache \
	ca-certificates \
    python3 \
    && python3 -m ensurepip \
    && apk add --update --no-cache \
        --repository "http://dl-cdn.alpinelinux.org/alpine/edge/testing" \
        --repository "http://dl-cdn.alpinelinux.org/alpine/edge/main" \
        libtorrent-rasterbar

RUN pip3 install --no-cache-dir --upgrade pip
RUN pip3 install --no-cache-dir --upgrade flexget transmissionrpc
RUN mkdir /root/.flexget
RUN mkdir /tmp/torrents

WORKDIR /opt/flexget

VOLUME ["/root/.flexget"]

ENTRYPOINT ["flexget"]