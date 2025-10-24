# Introduction

Example of a minimal docker compose project for prometheus, grafana, alert manager and pushgateway.

# Environment

Create a .env file at the root of the project.
Example of .env file:

```shell
COMPOSE_PROJECT_NAME=app-monitoring

GRAFANA_CONTAINER_NAME=app-monitoring-grafana
PROMETHEUS_CONTAINER_NAME=app-monitoring-prometheus
PUSHGATEWAY_CONTAINER_NAME=app-monitoring-pushgateway
ALERTMGR_CONTAINER_NAME=app-monitoring-alertmanager

GRAFANA_ADMIN_USER=grafana-admin-user
GRAFANA_ADMIN_PASSWORD=grafana-admin-password

ENVIRONMENT=production
PROMETHEUS_RETENTION_TIME=3d

```

# Deployment

To deploy the container, run the following command:

```shell
docker compose -f docker-compose-monitoring.yaml up -d --build
```

-d: detach mode, to avoid blocking the console and --build: to rebuild images on each deployment

# Official Documentation

- Prometheus, Alertmanager and Pushgateway: https://prometheus.io/docs/introduction/overview/
- Grafana: https://grafana.com/docs/
