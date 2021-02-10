# docker-commands

### List all container ids
```bash
docker ps -aq
```

### Stop all running containers
```bash
docker stop $(docker ps -aq)
```

### Remove all stopped containers
```bash
docker rm $(docker ps -aq)
```

### Docker stats to a file
```bash
 while true; do docker stats --no-stream >> data.txt; done
```
