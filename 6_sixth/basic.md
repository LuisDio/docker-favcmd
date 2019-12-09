Docker Compose

applicable to run only on single host

write a docker-compose.yml file
```
version '3'
services:
    redis:
      image: user/redis:1
    vote:
      image: user/web:1
      ports:
        - 5000:80
      links:
        - redis
    db:
      image: user/db:1
      ports:
        - 5001:80

    messaging:
      build: ./message - build image not already in registry
      ports:
        - 5002:80
```

```
docker-compose up - start the list of container
```

```
docker run --links - links container together
```

Example:
```
docker run -d --name=redis redis - this is the database required for communication
docker run -d --name=vote -p 5000:80 --link redis:redis voting-app - this allow use of redis within the application
```

```
docker use restart policy that can be added to docker-compose file: main policies are : "no", on-failure, always, unless-stopped
```
