# 39º Encontro DevOpsGo - SigNoz

## To start redis

`docker run --name some-redis -p 6379:6379 -d redis`

Check redis is running with: `docker ps`

## To start app

`node app.js`

## To start SigNoz using Docker

```
git clone -b main https://github.com/SigNoz/signoz.git && cd signoz/deploy/
docker-compose -f docker/clickhouse-setup/docker-compose.yaml up -d
```

SigNoz frontend [http://localhost:3301/](http://localhost:3301/)

## To start app with Open Telemetry instrumentation

`node -r ./tracing.js app.js`

## Using k6 to make some traffic

`k6 run k6.js`