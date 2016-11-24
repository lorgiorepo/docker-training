### Create image container and verify
```sh
$ docker build -t nodelor .
$ docker images
```

### Link to exist docker redis container
```sh
$ docker run -d -p 80:8080 --link redisio be9fe811f654
$ docker ps -a
```
