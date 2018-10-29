# Logstash Ingest Monitoring

Logging and Metrics stack using Docker containers, provisioning a dashboard
to monitor Logstash ingestion.

- [Logstash](https://www.elastic.co/products/logstash)
- [Elasticsearch](https://www.elastic.co/products/elasticsearch)
- [Kibana](https://www.elastic.co/products/kibana)
- [Graphite](https://graphiteapp.org/)
- [Grafana](https://graphiteapp.org/)

## Running

Bring up the stack,

```console
./up
```

(this will configure the elasticsearch environment and use `docker-compose` to provision the containters)

## Logstash

Logstash collects, parses and transforms logs before sending to Elasticsearch.

The [generator input plugin](https://www.elastic.co/guide/en/logstash/current/plugins-inputs-generator.html) is used to generate random log events and to publish event metrics to Graphite.

## Grafana UI

Grafana is used to configure the monitoring dashboard using Graphite metrics.

Navigate to http://grafana.docker.internal:3000 and login with the default `admin/admin`
credentials.

The dashboard is named `Logstash Ingest`.

## Kibana UI

The kibana UI can be used to view indexed logs - http://kibana.docker.internal:5601
