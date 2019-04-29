# Transmission

Builds a Docker image with the latest transmission version.

## Build
```console
$ make dockerbuild
```

## Publish
```console
$ make dockerpublish
```

## Usage

```console
$ docker run --rm \
        --name transmission \
        -v ~/projects/dockerfiles/transmission/config:/transmission/config \
        -p 9091:9091 \
        isaacasensio/transmission:1.0
```