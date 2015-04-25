# Xhprof image

## Requirements

You must have [Docker](https://www.docker.com/) >= 1.5.

## What's inside

This docker contains a clean [xhprof](http://xhprof.io/) install with [xhgui](https://github.com/perftools/xhgui).

### Configuration

### Ports

You can bind ports :

* 33333
* 27017
* 22

### Volumes

* /var/log/supervisor
* /var/log/nginx
* /var/log/php5-fpm
* /var/log/mongodb

## Usage

```bash
# pull (auto) and run
# mount volumes
docker run \
  -d \
  --name xhprof \
  -p 33333:33333 \
  -p 27017:27017 \
  -v /path/to/supervisor:/var/log/supervisor
  -v /path/to/nginx:/var/log/nginx
  -v /path/to/php5-fpm:/var/log/php5-fpm
  -v /path/to/mongodb:/var/log/mongodb
  monsieurchico/xhprof
```
