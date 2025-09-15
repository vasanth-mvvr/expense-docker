# So as the docker contains a default ip bridge . so there won't be communications with the other containers . so to overcome that we need to create a our own network where we need to place all the containers in that network.


To create network
```
docker network create <name>
```
To enter into the entry point
```
docker run -it --entrypoint /bin/bash <image:tag>
```