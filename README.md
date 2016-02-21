# docker-logstash-webdis

[![Deploy to Docker Cloud](https://github.com/yongjhih/docker-parse-server/raw/master/art/deploy-to-docker-cloud.png)](https://stackfiles.io/registry/56ca410523bc9401006b5aca)

## Usage

```sh
wget https://github.com/yongjhih/docker-logstash-webdis/raw/master/docker-compose.yml
chown :docker .
docker-compose up
```

* host:webdis:7379
* logstash.out
* host:kibana:5601

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
curl 'http://127.0.0.1:7379/LPUSH/logstash/\{"hello":"world"\}'
```
