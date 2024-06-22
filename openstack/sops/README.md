# Docker build

```
docker build -f <dockerfile> --build-arg VERSION=<sops-version> -t <tag>:<version> .
```

example :
```
docker build -f debian --build-arg VERSION=v3.8.1 -t docker.io/falltrades/openstack:sopsv3.8.1-debian12 .
docker build -f alpine --build-arg VERSION=v3.8.1 -t docker.io/falltrades/openstack:sopsv3.8.1-alpine3.20.0 .
```

