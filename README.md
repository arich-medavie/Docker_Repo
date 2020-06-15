# Docker_Repo
For Docker Training

## Docker Training : Commands


#### Notes
- only STDOUT & STDERR by default, are logged for the main process from a container (PID 1)

#### Generic Commands

```
systemd-cgtop

```

#### Docker Container
```
docker container run
  -it #interactive, terminal
  -d background from main tty
  exec <specific command>

docker container ls
  ls -a #lists even expired / stopped / quit containers
  ls -aq #lists only the container ID
  ls --filter "<string>"
  ls --no-trunc #non-truncated output

docker container top

docker container rm -f <container ID>

docker container logs <container ID>

```

#### Neat Tricks
```
# You can run a specific command string in a container: eg.
$ docker container run <image>:<tag> <command>
# ex.
$ docker container run centos:7 echo "Hello World"

# Reconnect to an exited container
docker container ls -a # find exited container ID
docker container start <container ID>
docker container exec -it <container ID> bash

# output container inspect to a human readable format
docker container inspect --format='{{json .<config object>}}' <container id> | jq


```

#### Container Listing
```
docker container ls

```
