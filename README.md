# docker-commands


### Stop all running containers
```bash
docker stop $(docker ps -aq)
```

### Remove all stopped containers
```bash
docker rm $(docker ps -aq)
```
