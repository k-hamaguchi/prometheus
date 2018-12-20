# Study for Prometheus

[PrometheusをDockerでさくっと動かしてコンテナで稼働するサービスの稼働監視](https://qiita.com/ike_dai/items/a1867a25e133bc8456d3)

## First Step

### Start Prometheus Server

```bash
docker run -p 9090:9090 -v $(pwd)/prometheus:/prometheus prom/prometheus --config.file=/prometheus/prometheus.yml
```

### Start node exporter

```bash
docker run -p 9100:9100 quay.io/prometheus/node-exporter
```

### View Dashboard

Access to `http://[Docker Host]:9090/`.

## Use Docker Compose

```bash
docker-compose up
```
