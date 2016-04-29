Remove dangling docker images
```
docker rmi --force $(docker images -f "dangling=true" -q)
```
