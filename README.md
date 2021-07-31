# Docker Compose

## Kafka + Zookeeper
- Is recommended to use `kafkacat` and create alias in your machine.
shell
```
alias kd='kafkacat -b localhost:29092'
```

## MySQL
- Just need to correctly add the volumes folder.
shell
```
docker run --name my-mysql -v /Users/murillo/dev/docker/docker-volumes/mysql:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=root -p 3306:3306 -d mysql:latest
```