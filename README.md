# docker-logstash-webdis

## Usage

```sh
wget https://github.com/yongjhih/docker-logstash-webdis/raw/master/docker-compose.yml
docker-compose up
```

* host:webdis:7379
* guest:redis:6379
* logstash.out, logstash.log, logstash.err

## Configuration

logstash.conf

environment:

- THREADS
- POOL_SIZE
- WEBSOCKETS
- ACL_DISABLED
- ACL_HTTP_BASIC_AUTH
- ACL_HTTP_BASIC_AUTH_ENABLED
- VERBOSITY
- LOGFILE
- DATABASE
- REDIS_HOST
- REDIS_PORT
- REDIS_AUTH

volumes:

- $PWD/webdis.log:/webdis.log

## Testing

```sh
curl http://127.0.0.1:7379/SET/hello/world
```
