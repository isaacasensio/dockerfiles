# flexget

Builds a Docker image with latest flexget version.

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
$ docker run \
    --link "transmission:transmission" \
    -v ~/your-config-folder:/root/.flexget \
    isaacasensio/flexget:latest \
    execute
```

