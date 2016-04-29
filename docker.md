Remove dangling docker images
```
docker rmi --force $(docker images -f "dangling=true" -q)
```

Remove containers that have not been used since weeks ago (change to x days ago if needed)
```
docker rm $(docker ps -a | grep 'weeks ago' | awk '{print $1}')
```