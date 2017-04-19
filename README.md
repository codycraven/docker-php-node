# PHP/Node.js Alpine Docker image

## Image usage

See the documentation for the image on
[Docker Hub](https://hub.docker.com/r/codycraven/php-node/).

## How to build new images

Run `build` with the semantic PHP version and Node.js versions (in that order)
as arguments.

Example:

```bash
# ./build PHP_VERSION NODE_VERSION
./build 7.1.4 7.9.0
```

_Major, minor, and latest tags will automatically be tagged if the versions
provided are detected to meet such criteria._