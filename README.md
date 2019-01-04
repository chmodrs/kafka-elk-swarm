# kafka-elk-docker-swarm

Deploy ELK stack with kafka for buffer logs collection in Docker Swarm Cluster.

1- create esdata directory and put config files in each swarm node or create a shared volume

2- run kafka stack

docker stack deploy -c docker-compose-kafka.yml kafka

3- run elk stack

docker stack deploy -c docker-compose-elk.yml elk
