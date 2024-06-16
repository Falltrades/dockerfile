# Docker build

```
docker build -f <dockerfile> --build-arg VERSION=<version> -t <tag>:<version> .
```

example :
```
docker build -f debian --build-arg VERSION=v1.30.1 -t docker.io/falltrades/cloud-pi-native:v1.30.1-debian12 .
docker build -f alpine --build-arg VERSION=v1.30.1 -t docker.io/falltrades/cloud-pi-native:v1.30.1-alpine3.20.0 .
```

