# stresst - run "stress-ng" command over REST-like I/F


# prerequisites

- some kind of container platform ( i.e. Docker, Kubernetes, ...)

# usage

## run

```
sudo docker run --rm -p 8080:8080 stresst 
```

## build

```
sudo docker build . -t stresst
```

```
# License
MIT

# CI

[![CircleCI](https://circleci.com/gh/hrkt/greetings-server.svg?style=svg)](https://circleci.com/gh/hrkt/stresst)
