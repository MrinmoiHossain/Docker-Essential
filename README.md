# Docker Information

## Installation on Linux (debian)
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

## Check Version
- print out full details of docker server and clients: ```$ docker version```
- print out only docker server version: ```$ docker version --format '{{.Server.Version}}'```


## Container Management Commands
#### Status
- show a list of running containers : ```$ docker ps``` or ```$ docker container ls```
- show a list of all containers : ```$ docker ps -a``` or ```$ docker ps --all``` or ```$ docker container ls -a```
#### Create
- create a new container from an image : ```$ docker create IMAGE```
#### Start
- start a container after create : ```$ docker start -a ID```
- start a stopped container : ```$ docker start ContainerID``` or ```$ docker start ContainerName```
#### Run
- start a new container from an image : ```$ docker run Image```
- start a new container from an image and change default commands : ```$ docker run Image Commands```
- start a new container from an image and assign it a name : ```$ docker run --name Name Image```
- start a new container from an image and run in the background : ```$ docker run -d Image```
- start a new container from an image and map all ports : ```$ docker run -p HostPort:DockerPort Image```
#### Pause / Unpause / Wait
- 
- 
#### Stop / Kill
- stop a running container : ```$ docker stop ContainerID``` or ```$ docker stop ContainerName```
- kill a running container : ```$ docker kill ContainerID``` or ```$ docker stop ContainerName```
#### Restart
- restart a container : ```$ docker restart ContainerID``` or ```docker start ContainerName```
#### Delete
- delete a container : ```$ docker rm ContainerID``` or ```docker rm ContainerName```
- delete a running container : ```$ docker rm -f ContainerID``` or ```docker rm -f ContainerName```
- delete stopped containers : ```$ docker container prune```
