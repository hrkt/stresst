# stresst - run "stress-ng" command over REST-like I/F


# prerequisites

- some kind of container platform ( i.e. Docker, Kubernetes, ...)

# usage

## run server

```
sudo docker run --rm -p 8080:8080 stresst 
```

## try adding stress to OS

```
curl http://localhost:8080/usr/bin/stress-ng?--cpu&1&-l&50&-t&15s
```



# dev

## build

```
sudo docker build . -t stresst
```

```
# License
MIT

# CI

[![CircleCI](https://circleci.com/gh/hrkt/greetings-server.svg?style=svg)](https://circleci.com/gh/hrkt/stresst)
