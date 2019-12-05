Docker Engine

-- Docker Deamon --> background process that manage images, containers, volume ...

-- REST API      --> API that can be used by other program to talk to the Deamon

-- Docker CLI    --> command line interface


```
docker -H=remote-docker-engine:2375 - Access a remote docker engine
docker -H=10.123.2.1:2375 run nginx - run a container remotely
```

Docker use cgroup to restrict the amount of resources allocated
```
docker run --cpus=.5 ubuntu
docker run --memory=100m ubuntu
```
