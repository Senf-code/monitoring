# Monitoring Stack with Docker Compose

## Описание проекта

Этот проект предоставляет полный стек мониторинга для Linux-серверов. Система собирает метрики CPU, RAM, диска и сети, а также мониторит потребление ресурсов и состояние контейнеров Docker. 

**Основные компоненты:**
- **Node Exporter** - собирает метрики хост-системы
- **Prometheus** - агрегирует, хранит и алертит метрики
- **Grafana** - визуализирует метрики в удобном интерфейсе
- **Cadvisor** - мониторит состояние и потребление ресурсов контейнеров

## Stack

* Docker
* Docker Compose
* Prometheus
* Grafana
* Node Exporter
* Cadvisor
* Linux

## Architecture

```text
Node Exporter ──> Prometheus ──> Grafana
```

* Node Exporter собирает метрики хоста
* Prometheus собирает и хранит метрики
* Grafana визуализирует мониторинг данных

## Screenshots

### Grafana Dashboard Overview

![Overview](screenshots/grafana-overview.png)

### Storage & Disk Metrics

![Storage](screenshots/grafana-storage.png)

### Network traffic

![Network traffic](screenshots/grafana-network-traffic.png)

### Prometheus Targets

![Prometheus Targets](screenshots/prometheus-targets.png)

### Docker containers

![Docker containers](screenshots/docker-ps.png)

## Quick Start

```bash
git clone https://github.com/Senf-code/monitoring.git
cd monitoring
cp .env.example .env
docker compose up -d
```
