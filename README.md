### The container image PHP 7.4 / CLI, FPM, and Swoole for arm64/v8 platform

This image overrides Ubuntu's PHP packages with Ondřej's to ensure I always have the very latest. For instance, Ubuntu 20.04 comes with php 7.4.3 but I still install 
[Ondřej's](https://github.com/oerdnj/deb.sury.org) packages to ensure I get the absolutest latest version of php 7.4 every time. Ubuntu backport security fixes, but not necessarily bugfixes from later patch releases.

I use it for [archlinux.org.ua](https://archlinux.org.ua) project.

```bash
docker pull onuk/php7.4-fpm:0.0.1
docker run --rm -t -p 9000:9000 -v $(pwd):/app onuk/php7.4-fpm:0.0.1 php
```
