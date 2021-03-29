# dockerswarm
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

https://github.com/dockersamples/docker-swarm-visualizer
docker run -it -d -p 8080:8080 -v /var/run/docker.sock:/var/run/docker.sock dockersamples/visualizer




work:
docker swarm join --token SWMTKN-1-5r3ktwewh2fpj3ricvy4aaa6lxagnrpweqjdk4iuo7zkyqs51v-789fz0r6na1x5i5z4bzr6nq5v 192.168.1.213:2377

