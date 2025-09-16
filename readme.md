# So as the docker contains a default ip bridge . so there won't be communications with the other containers . so to overcome that we need to create a our own network where we need to place all the containers in that network.


To create network
```
docker network create <name>
```
To enter into the entry point
```
docker run -it --entrypoint /bin/bash <image:tag>
```

# **To remove cache**
```
docker system prune -a 
```
```
docker builder prune  
```
```
docker image prune 
```
# **To see intermediate layers running**
```
export DOCKER_BUILDKIT=0
```

# **To push the images **
```
docker login
```
* Rename the tag before push
```
docker tag <old image name> <new image name>
```
```
docker push <image name>
```