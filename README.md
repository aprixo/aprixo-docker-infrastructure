# aprixo-docker-infrastructure

This project deploays a full webstack with nginx, php, mysql, mongodb, memcached and elasticsearch using host volumes to store data. We provide this as a development environment for local development.

Also you can use this as a full PHP Webstack for other projects.

See https://github.com/aprixo/aprixo-os for more details on aprixo.

The stack is using the official images form the following projects:

nginx
mongodb
memcached
mysql
php

php has a tailored build with a huge set of (use(able|d)) extensions and its own dockerfile.

## getting started Local Development

To start with this environment, you need some preparations.

Add 
```
127.0.0.1   *.localhost 
```

to your /etc/hosts file. (Asuming you develop with an unix like system / on linux)
 
Add /srv/www and /srv/docker/apstack directories

copy the conf directory to /srv/docker/apstack/

checkout your aprixo application to /srv/www/vhost/yourdirectory/

adjust the aprixo.conf in the conf/nginx/sites-available directory to your local path.

add a symlink from sites-enabled/aprixo.conf to sites-available/aprixo.conf

Boot your docker stack.

## getting started as server

TODO: live server steps...