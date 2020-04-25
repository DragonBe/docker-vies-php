# Docker packages for VIES

This repository contains Docker container images used for testing my [dragonbe/vies](https://packagist.org/packages/vies) composer package.

They are based off the official [php](https://hub.docker.com/_/php) container images with the addition of the `php-soap` extension.

## Usage

Go to the project root of your vies installation and run the container straight from the commandline.

```sh
docker run -it --rm --name vies-test -v "$PWD":/usr/src/myapp -w /usr/src/myapp dragonbe/vies-php:7.4-cli vendor/bin/phpunit --no-coverage
```

These containers are provided as-is and are licensed under a [MIT licence](LICENSE).
