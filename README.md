# Docker Compose

## Kafka + Zookeeper
- Is recommended to use `kafkacat` and create alias in your machine.
shell
```
alias kd='kafkacat -b localhost:29092'
alias kafkaOn='docker-compose -f {path}/docker-compose-kafka-zookeeper.yaml up -d'
alias kafkaOff='docker-compose -f {path}/docker-compose-kafka-zookeeper.yaml down'
```

## MySQL
- Just need to correctly add the `volumes` folder.
shell
```
docker run --name my-mysql -v /Users/murillo/dev/docker/docker-volumes/mysql:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=root -p 3306:3306 -d mysql:latest
```

## PostgreSQL
- Just need to correctly add the `volumes` folder.
shell
```
docker run --name my-postgresql -v /Users/murillo/dev/docker/docker-volumes/postgresql:/var/lib/postgresql/data -e POSTGRES_PASSWORD=root -p 5432:5432 -d postgres:latest
```
