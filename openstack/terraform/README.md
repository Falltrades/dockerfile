# Docker build

```
docker build -f <dockerfile> --build-arg VERSION=<terraform-version> -t <tag>:<version> .
```

example :
```
docker build -f debian --build-arg VERSION=1.8.5 -t docker.io/falltrades/openstack:terraform1.8.5-debian12 .
docker build -f alpine --build-arg VERSION=1.8.5 -t docker.io/falltrades/openstack:terraform1.8.5-alpine3.20.0 .
```

