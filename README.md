# PHP/Node.js Alpine Docker image

## Image usage

See the documentation for the image on
[Docker Hub](https://hub.docker.com/r/codycraven/php-node/).

## How to build new images

Run `build` with the semantic PHP version and Node.js versions (in that order)
as arguments:

```bash
# ./build PHP_VERSION NODE_VERSION
./build 7.1.4 7.9.0
```

### Build options

Build options are managed through environment variables.

#### Also tag images as latest

```bash
LATEST=1 ./build 7.1.4 7.9.0
```

#### Use your own namespace (instead of codycraven)

```bash
NAMESPACE=yournamespace ./build 5.6.30 6.10.2
