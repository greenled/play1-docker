# Play Framework 1.x docker development images

https://hub.docker.com/r/greenled/play1

For those who still use [Play! Framework 1.x](https://www.playframework.com/documentation/1.5.x/home) series, like me :)

## How to use

Run with `-it` options, publish port 9000 (or whatever port your app is running on) and bind the project directory as a volume. Also, to avoid file permission issues, run as the current user.

```bash
docker run -it -p 9000:9000 -v `pwd`:`pwd` -e IVY_HOME=`pwd`/.ivy2 -w `pwd` -u `id -u`:`id -g` greenled/play1:1.5.1
```

I made this image in a hurry, and it's working well so far, but it needs some polishing for sure. Feedback is welcome.
