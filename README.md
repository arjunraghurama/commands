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
