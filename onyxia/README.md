# Docker build

```
docker build --build-arg -t <tag>:<version> .
```

example :
```
DOCKER_BUILDKIT=1 docker build --build-arg FORGEDOMAIN=$FORGEDOMAIN --build-arg APTDOMAIN=$APTDOMAIN --build-arg USER=$ORIONUSER --build-arg PASS=$ORIONPASS --build-arg PROXY=$PROXY --build-arg NO_PROXY=$no_proxy -t falltrades/onyxia-vscode-python:py3.12.4 .
```

