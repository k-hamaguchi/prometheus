# Study for Prometheus

[PrometheusをDockerでさくっと動かしてコンテナで稼働するサービスの稼働監視](https://qiita.com/ike_dai/items/a1867a25e133bc8456d3)

## First Step

### Start Prometheus Server

```bash
docker run -p 9090:9090 -v $(pwd)/prometheus-data:/prometheus-data prom/prometheus --config.file=/prometheus-data/prometheus.yml
```

### Start node exporter

```bash
wget https://github.com/prometheus/node_exporter/releases/download/v0.16.0-rc.1/node_exporter-0.16.0-rc.1.linux-amd64.tar.gz
tar xvzf node_exporter-0.16.0-rc.1.linux-amd64.tar.gz
cd node_exporter-0.16.0-rc.1.linux-amd64
./node_exporter
```

### View Dashboard

Access to `http://[Docker Host]:9090/`.
