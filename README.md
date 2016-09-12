# boot-openjdk-clj-docker-image

This is an unofficial boot clojure docker image.

This image installs and sets up the latest version of [Boot][boot] and runs on top of
[OpenJDK 8][openjdk] image.

This is an [automated build][docker] in Docker Hub. The
`ignorabilis/boot-openjdk-clj` Docker image is automatically built from the _Dockerfiles_
in this repo (under jessie and alpine, respectively).

## Important

Pieces used from [boot-clj-docker-image][boot-clj-docker-image] and [docker-clojure][docker-clojure].

## Test

```
$ docker run -it ignorabilis/boot-openjdk-clj:alpine repl
```

## Usage

To use this image for your app or for another image put this at the top of your
_Dockerfile_: 

    FROM ignorabilis/boot-openjdk-clj:alpine


[boot]:   https://github.com/boot-clj/boot
[docker]: https://docs.docker.com/docker-hub/builds
[openjdk]: https://hub.docker.com/_/openjdk/
[boot-clj-docker-image]: https://github.com/adzerk-oss/boot-clj-docker-image
[docker-clojure]: https://github.com/Quantisan/docker-clojure
