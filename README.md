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
$ docker run ubuntu sleep 5
$ docker run ubuntu exec cat /etc/hosts
$ docker run -d nginx
$ docker attach container_id
$ docker run redis:4.0
$ docker run -i image_name
$ docker run -it image_name
$ docker run -p 80:8080 nginx				[-p host_port:container_port]
$ docker run -v /opt/datadir:/var/lib/mysql mysql	[-v host_addr:container_addr]
$ docker run -e VAR_NAME=Value nginx
$ docker run ubuntu --network=none
$ docker run ubuntu --network=host
$ docker run -v volume_name:/var/lib/mysql mysql
$ docker run --mount type=bind,source=/data/mysql,target=/var/lib/mysql mysql
$ docker run -d --name=name -p 5000:80 --link redis:redis python
$ docker run --cpu=.5 ubuntu
$ docker run --memory=100m ubuntu
```