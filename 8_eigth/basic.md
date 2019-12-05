Docker Storage

Docker file system
```
/var/lib/docker
```

```
docker volume create data_volume - create volume within the file system(optional)
```
```
/var/lib/docker/volume/data_volume
```

```
docker run -v data_volume:/var/lib/mysql mysql - volume mounting
docker run -v data_volume2:/var/lib/mysql mysql
docker run -v /data/mysql:/var/lib/mysql mysql - bind mount(from any location on the host)

```

New way of doing
```
docker run \
--mount type=bind,source=/data/mysql,target=/var/lib/mysql mysql
```
