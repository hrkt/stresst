# stresst - run "stress-ng" command over REST-like I/F

[stress-ng](https://kernel.ubuntu.com/~cking/stress-ng/), is a package for running stress test on OS, platform.

With this "REST-like wrapper", you can run stress-ng over HTTP.

ex) running this in your shell, a stress test of "50% load - 1cpu test - for 15 seconds"
 
```
curl http://localhost:8080/usr/bin/stress-ng?--cpu&1&-l&50&-t&15s
```

more examples for stress-ng parameters are [here](https://wiki.ubuntu.com/Kernel/Reference/stress-ng).

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
