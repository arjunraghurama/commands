# bash-commands
### mount a drive
fdisk is a command line utility to view and manage hard disks and partitions on Linux systems
```bash
fdisk -l 
```

To partition a particular hard disk, for example /dev/sdb.
Commonly used fdisk commands.

    n – Create partition
    p – print partition table
    d – delete a partition
    q – exit without saving the changes
    w – write the changes and exit.

```bash
fdisk /dev/sdb
```
Format the disk with mkfs command
```bash
mkfs.ext4 /dev/sdb
```

mount the partition
```bash
mount /dev/sdb /data
```

Make an entry in /etc/fstab file for permanent mount at boot time
```bash
/dev/sdb  /data  ext4  defaults  0  0
```
---

### rename all files in sequential order
```bash
ls | cat -n | while read n f; do mv "$f" "file-$n.<extension>"; done
```

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
