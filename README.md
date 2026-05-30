# Monitoring Stack with Docker Compose

## Stack

* Docker
* Docker Compose
* Prometheus
* Grafana
* Node Exporter
* Linux

## Architecture

```text
Node Exporter ---> Prometheus ---> Grafana
```

* Node Exporter collects host metrics
* Prometheus scrapes and stores metrics
* Grafana visualizes monitoring data

## Screenshots

### Grafana Dashboard Overview

![Overview](screenshots/grafana-overview.png)

### Storage & Disk Metrics

![Storage](screenshots/grafana-storage.png)

### Network traffic

![Network traffic](screenshots/grafana-network-traffic.png)

### Prometheus Targets

![Targets](screenshots/prometheus-targets.png)

### Docker containers

![Docker containers](screenshots/docker-ps.png)

## Quick Start

```bash
git clone https://github.com/Senf-code/monitoring.git
cd monitoring
cp .env.example .env
docker compose up -d
```
