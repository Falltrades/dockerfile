# Docker build

```
docker build -f <dockerfile> --build-arg VERSION=<version> -t <tag>:<version> .
```

example :
```
docker build -f debian --build-arg VERSION=1.8.5 -t docker.io/falltrades/openstack:1.8.5 .
docker build -f alpine --build-arg VERSION=1.8.5 -t docker.io/falltrades/openstack-alpine:1.8.5 .
```

