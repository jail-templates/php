# PHP
Bastille template to install and configure the latest stable php-fpm with some sane defaults.

* Contains PHP extensions required for applications like Wordpress and Nextcloud.
* Runs on a Unix socket instead of TCP port 9000 for added security and performance.
* Has user configurable PHP settings in `/usr/local/etc/php/custom.ini`.
* Generates `info.php` in the webroot. Make sure to remove this file in production.
* Support for PHP OPcache and APCu caching.

## Requirements
Requires the Apache HTTP Server, for which templates are available as well.

## Bootstrap
```
bastille bootstrap https://github.com/jail-templates/php
```

## Apply template
```
bastille template $JAIL jail-templates/php
```

## Upgrading PHP
Another PHP template can be applied on a jail to upgrade or downgrade the PHP version. For example: $JAIL had the `php-8.0` template applied to it and by applying the `php-8.2` template the PHP version upgrades to 8.2. Make sure to backup your custom settings in `/usr/local/etc/php/custom.ini` though because they will be overwritten to the default settings as well.

## Support
Templates will be maintained until their respective software version is end-of-life. Repositories will then be archived and removed from any meta-templates.

If you have a question, suggestion or find a bug, please let us know via an Issues in the relevant repository or send us an email.

## License
All templates are distributed under the 3-Clause BSD License. See `LICENSE` in every template repository for more information.
