All tags for this image are based on Alpine with PHP and Node.js support. The image starts by using the official [PHP](https://hub.docker.com/_/php/) Alpine image. It then pulls in the Dockerfile from the official [Node.js](https://hub.docker.com/_/node/) Alpine image and build it atop the PHP image.

## Tags

Since the image is built on Alpine, multiple tag variations are provided to give the basic tools needed for building your projects.

- *-volume

    Creates a volume for the Yarn cache directory. Massively speeds up `yarn` commands between container instances.

- *-git

    Includes git in the image, allowing cloning from remote repositories.

- *-volume-git

    Includes both the Yarn cache directory volume and git.

## Purpose

While not best practice, it is once in a while necessary to include two different processes within a single Docker container. I ran into this issue when attempting to use Pattern Lab _(Node.js)_ with Twig _(PHP)_ templates.

## Building Your Own

If you need to use a PHP/Node version combination that is not included in the tags available on Docker Hub, you can [build your own](https://github.com/codycraven/docker-php-node).