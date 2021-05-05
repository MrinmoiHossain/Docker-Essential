# Docker Information

## Installation on linux (debian)
```bash
$ sudo apt-get install docker.io
$ sudo systemctl status docker.service
$ sudo groupadd docker
$ sudo usermod -aG docker $USER
$ newgrp docker
$ docker version
$ sudo apt-get install docker-compose
$ docker-compose version
```

## Check docker version
- print out full details of docker server and clients: ```$ docker version```
- print out only docker server version: ```$ docker version --format '{{.Server.Version}}'```


