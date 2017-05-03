All tags for this image are based on Alpine with PHP and Node.js support. The image starts by using the official [PHP](https://hub.docker.com/_/php/) Alpine image. It then pulls in the Dockerfile from the official [Node.js](https://hub.docker.com/_/node/) Alpine image and builds it atop the PHP image.

## Tags

The tags for this image are broken into two types, main and builder. [View all tags](https://hub.docker.com/r/codycraven/php-node/tags/).

Examples:

- Main tags:
    - [`codycraven/php-node:latest` _(main/Dockerfile)_](https://github.com/codycraven/docker-php-node/main/Dockerfile)
    - `codycraven/php-node:php-7.1.4--node-7.9.0`
- Builder tags:
    - [`codycraven/php-node:latest--builder` _(builder/Dockerfile)_](https://github.com/codycraven/docker-php-node/builder/Dockerfile)
    - `codycraven/php-node:php-7.1.4--node-7.9.0--builder`


Main tags include the PHP and Node version they are named after. They also include the latest [Yarn](https://yarnpkg.com/en/) and [Composer](https://getcomposer.org/) from the time of the build.

Builder tags extend the main tag their name matches but also include additional common build dependencies that may be encountered when performing an `npm install`, `yarn install`, or `composer install`. Additional packages _(note Alpine version will be based on the [PHP](https://hub.docker.com/_/php/) Alpine image extended from)_:

- [build-base](https://pkgs.alpinelinux.org/package/v3.4/main/x86_64/build-base):
    - binutils
    - fortify-headers
    - g++
    - gcc
    - libc-dev
    - make
- [git](https://pkgs.alpinelinux.org/package/v3.4/main/x86_64/git)
- [python 2.7](https://pkgs.alpinelinux.org/package/v3.4/main/x86_64/python)

## Purpose

While not best practice, it is once in a while necessary to include two different processes within a single Docker container. I ran into this issue when attempting to use Pattern Lab _(Node.js)_ with Twig _(PHP)_ templates.

## Building Your Own

If you need to use a PHP/Node version combination that is not included in the tags available on Docker Hub, you can [build your own](https://github.com/codycraven/docker-php-node).