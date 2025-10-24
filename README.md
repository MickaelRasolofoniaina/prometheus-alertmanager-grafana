# Introduction

Exemple d'un projet docker compose minimaliste pour prometheus, grafana, alert manager et pushgateway.

# Environnement

Créer un fichier .env à la racine du projet.
Exemple de fichier .env

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

# Déploiement

Pour déployer le conteneur, exécuter la commande suivante:

```shell
docker compose -f docker-compose-monitoring.yaml up -d --build
```

-d: detach mode, pour ne pas bloquer la console et --build: pour régénerer les images à chaque déploiement

# Documentation officielle

- Prometheus, Alertmanager et Pushgateway: https://prometheus.io/docs/introduction/overview/
- Grafana: https://grafana.com/docs/
