# NTP with DDoS potential

This image provides a misconfigured ntp service. The service will respond to
mode 6 and mode 7 packages, which can be used in amplifications attacks.

## Build the container

```
$ podman build -t vuln-ntp .
```

## Start the container

```
docker run --rm -d --name dying-ntp -p 123:123/udp vuln-ntp:latest
```

## Stop the container

```
$ docker stop dying-ntp
```

