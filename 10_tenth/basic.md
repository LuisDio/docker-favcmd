Container orchestration

Used for: <br/>
-- scalability <br/>
-- load balancing <br/>
-- scalability <br/>
-- scalability <br/>


Docker Swarm - combining multiple docker machine together to a single cluster<br/>
             - swarm will take care of distributing application instances to separate host
             - for availability and for load balancing across different system and hardware
<br/>

To set a docker swarm orchestration you must have multiple host machine with docker installed<br/>
Then one machine must be the Swarm Manager and other must be slave machine <br/>

```
docker swarm init - initialize the swarm Manager(on the swarm manager)
```

```
docker swarm join --token <token> - join slave to the master with generated token from master(on docker node slave)
```




```
docker service create --replicas=3 my-web-server - run my-web-server on 3 instances slave across the cluster(must be run on manager node)
```
