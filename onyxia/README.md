# Docker build

```
docker build --build-arg -t <tag>:<version> .
```

example :
```
awk -F\" '{print "export " $2}' /etc/systemd/system/docker.service.d/http-proxy.conf | grep PROXY > /tmp/secret.txt
echo "export APTDOMAIN=${APTDOMAIN}" >> /tmp/secret.txt
echo "export FORGEDOMAIN=${FORGEDOMAIN}" >> /tmp/secret.txt
DOCKER_BUILDKIT=1 docker build --secret id=https_proxy,src=/tmp/secret.txt . -t falltrades/onyxia-vscode-python:py3.12.4
```

