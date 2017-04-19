centos-base
===========

This is a basic Centos 7 docker image.
It contains mostly the mandatory tools.

Prerequisites
-------------

- Docker

Usage
-----

```text
docker pull yueyehua/centos-base
docker run \
  -d \                                           # daemonize
  --privileged \                                 # for systemd
  -v /sys/fs/cgroup:/sys/fs/cgroup:ro \          # for systemd
  --name base \                                  # container name
  -h base \                                      # hostname
  yueyehua/centos-base
docker exec -ti base bash
[Do something here]
docker stop base
docker rm base
```
