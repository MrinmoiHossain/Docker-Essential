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
- start a new container from an image and removes a container after it exits : ```$ docker run --rm Image```
#### Pause / Unpause / Wait
- suspends all processes in the specified containers : ```$ docker pause ContainerID``` or ```$ docker pause ContainerName```
- un-suspends all processes in the specified containers : ```$ docker unpause ContainerID``` or ```$ docker unpause ContainerName```
- block until one or more containers stop and then print their exit codes : ```$ docker wait ContainerID``` or ```$ docker wait ContainerName```
#### Stop / Kill
- stop a running container : ```$ docker stop ContainerID``` or ```$ docker stop ContainerName```
- kill a running container : ```$ docker kill ContainerID``` or ```$ docker stop ContainerName```
#### Restart
- restart a container : ```$ docker restart ContainerID``` or ```docker start ContainerName```
#### Delete
- delete a container : ```$ docker rm ContainerID``` or ```docker rm ContainerName```
- delete a running container : ```$ docker rm -f ContainerID``` or ```docker rm -f ContainerName```
- delete stopped containers : ```$ docker container prune```
#### Rename
- rename a container : ```$ docker rename ContainerName NewContainerName```
#### Update
- update the configuration of one or more containers : ```$ docker update ContainerName```
#### Attach
- attach local standard input, output, and error streams to a running container : ```$ docker attach ContainerID``` or ```$ docker attach ContainerName```
#### Information
- show the container output (stdout & stderror) : ```$ docker logs ContainerID``` or ```$ docker logs ContainerName```
- show low level information on the container : ```$ docker inspect ContainerID``` or ```$ docker inspect ContainerName```
- list the process running inside the container : ```$ docker top ContainerID``` or ```$ docker top ContainerName```
- to get real-time events from the server : ```$ docker events```
- list port mappings or a specific mapping for the container : ```$ docker port ContainerID``` or ```$ docker port ContainerName```
- display a live stream of container(s) resource usage statistics : ```$ docker stats```
- inspect changes to files or directories on a container’s filesystem : ```$ docker diff ContainerID``` or ```$ docker diff ContainerName```
