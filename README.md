# zetifi-docker-nfdump

Alpine Linux Dockerfile that contains the nfdump tools.

## Updating the image

```
$ docker build . -t zetifi/nfdump -t zetifi/nfdump:latest
$ docker push zetifi/nfdump
```

## Using

You can use all the available nfdump tools (see: http://nfdump.sourceforge.net/) in a `docker-compose` like the following:

```
version: "3.1"
services:
  nfcapd:
    image: zetifi/nfdump
    restart: always
    command: nfcapd ...
  nfdump:
    image: zetifi/nfdump
    command: nfdump ...
  ...
```
