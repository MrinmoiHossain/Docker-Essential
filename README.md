# Docker Essential For DevOps

```bash
$ docker version
$ docker run nginx
$ docker ps
$ docker ps -a
$ docker images
$ docker container ls -a
```

### Docker Container
```bash
$ docker container ls -a
$ docker stop container_id/container_name
$ docker rm container_id/container_name
```

### Docker Image
```bash
$ docker images -a
$ docker pull image_name
$ docker rmi image_name
$ docker rmi $(docker images -a -q)
$ docker rmi -f $(docker images -a -q)
```

### Docker Run
```bash

```