# Logstash Ingest Monitoring

Logging and Metrics stack using Docker containers, provisioning a dashboard
to monitor Logstash ingestion.

- Logstash
- Elasticsearch
- Kibana
- Graphite
- Grafana

## Running

Bring up the stack,

```console
./up
```

## Grafana UI

Navigate to http://grafana.docker.internal:3000 and login with the default `admin/admin`
credentials.

The dashboard is `Logstash Ingest`.

## Kibana UI

The kibana UI can be used to view indexed logs - http://kibana.docker.internal:5601
