# kafka-elk-docker-swarm

Deploy ELK stack with kafka for buffer logs collection in Docker Swarm Cluster.

1- create overlay network "elk-network"
```
# docker network create -d overlay --attachable elk-network
```
2- create esdata directory and put config files in each swarm node or create a shared volume

3- run kafka stack
```
docker stack deploy -c docker-compose-kafka.yml kafka
```
4- run elk stack
```
# docker stack deploy -c docker-compose-elk.yml elk
```
