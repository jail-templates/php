# PHP 8.3
Bastille template to install and configure php-fpm with some sane defaults.

* Contains PHP extensions required for applications like Wordpress and Nextcloud.
* Runs on a Unix socket instead of TCP port 9000 for added security and performance.
* Has user configurable PHP settings in `/usr/local/etc/php/custom.ini`.
* PHP OPcache and APCu caching are enabled by default.

## Requirements
Requires the Apache HTTP server, for which templates are available as well.

## Bootstrap
```
bastille bootstrap https://github.com/jail-templates/php-8.3
```

## Apply template
```
bastille template $JAIL jail-templates/php-8.3
```
