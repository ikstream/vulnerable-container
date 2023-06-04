# NTP with DDoS potential

This image provides a misconfigured ntp service. The service will respond to
mode 6 and mode 7 packages, which can be used in amplifications attacks.

## Build the container

```sh
$ docker build --tag vuln-ntp .
```

## Start the container

```sh
docker run --rm --detach --name dying-ntp --publish 123:123/udp vuln-ntp:latest
```

## Stop the container

```sh
docker stop dying-ntp
```

