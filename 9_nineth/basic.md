Docker Networking

Default Network created at install are:<br/>
--- Bridge - private internal network created by docker on the host in range 172 <br/>
--- None - no network setting attached( Not accessible at all) <br/>
--- host

```
docker run ubuntu - use bridge as default network(container can access each other IP if required)
```
To access them outside, need to map their internal port to host port.<br/>
Another way is to associate them to host network <br/>

We could create our own network for few container to be isolated like so
```
docker network create \
  --driver bridge \
  --subnet 182.18.0.0/16 \
  --gateway 182.18.0.1
  custom-isolated-network
```

```
docker run ubuntu --network=none - use none as network setting(isolated network)
```

```
docker run ubuntu --network=host - use host network setting
```

```
docker image ls - list images
docker container ls - list container
docker network ls - list network
```


inspect Network

```
docker inspect containe_name_or_id - then find network
```
```
docker inspect network_id - inspect the network setting
```

Container can reach other using their container name(or internal IP not ideal though) through the builtin DNS
