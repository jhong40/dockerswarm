# dockerswarm

- [swarm visualizer](https://github.com/dockersamples/docker-swarm-visualizer)
- [swarm deploy stack / docker-compose](https://docs.docker.com/engine/swarm/stack-deploy/)
```
docker run -it -d -p 8080:8080 -v /var/run/docker.sock:/var/run/docker.sock dockersamples/visualizer
```

```
manager:
docker swarm init
docker swam join-token worker  #in case forget the token
docker node ls

docker service create --name webapp1 --replicas=6 nginx  # webapp1 is the task
docker servie ls

-autolock
docker swarm init --autolock  # when init
docker swarm update --autolock=true  # after init

docker info # manager node, how many node



docker inspect:
root@web:~# root@web:~# docker service ls
ID                  NAME                MODE                REPLICAS            IMAGE               PORTS
dw5noqty39be        webapp1             replicated          6/6                 nginx:latest
docker inspect webapp1 
docker inspect dc74 # inspect docker ip address, default gateway, part of service


docker stack deploy --compose-file docker-compose.yml stackdemo
docker stack services stackdemo
docker stack rm stackdemo
docker service rm registry
docker swarm leave --force




worker:
docker swarm join --token SWMTKN-1-5r3ktwewh2fpj3ricvy4aaa6lxagnrpweqjdk4iuo7zkyqs51v-789fz0r6na1x5i5z4bzr6nq5v 192.168.1.213:2377
```
