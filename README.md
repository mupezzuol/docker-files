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
docker run --name my-mysql -v /Users/{computer-user}/dev/docker/volumes/mysql:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=root -p 3306:3306 -d mysql:latest
```

## PostgreSQL
- Just need to correctly add the `volumes` folder.
shell
```
docker run --name my-postgresql -v /Users/{computer-user}/dev/docker/volumes/postgresql:/var/lib/postgresql/data -e POSTGRES_PASSWORD=root -p 5432:5432 -d postgres:latest
```

## MongoDB
- Just need to correctly add the `volumes` folder.
shell
```
docker run --name my-mongodb -v /Users/{computer-user}/dev/docker/volumes/mongodb:/data/db -e MONGO_INITDB_ROOT_USERNAME=root -e MONGO_INITDB_ROOT_PASSWORD=root -p 27017:27017 -d mongo:latest
```