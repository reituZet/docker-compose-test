# Docker-compose.test

Задание:
1. Установить docker, docker-compose
2. Найти готовые контейнеры и запустить через docker-compose связку mariadb+wordpress+apache
3. Активировать плагин mod_status для mariadb+wordpress+apache
4. Найти готовые контейнеры и запустить связку prometheus+grafana
5. Настроить prometheus на мониторинг apache через mod_status и добавить в graphana готовый дашборд [dashboard](https://grafana.com/grafana/dashboards/9675)

## Структура

1. docker-compose.yaml - основной конфиг развёртывания контейнеров.
2. ./prometheus/config/prometheus.yaml - конфигурационный файл Prometheus
3. ./grafana/dashboards/AutoImported - дашборды для Grafana
4. ./apache-configs/010-status.conf - конфиг-файл для mod_status apache

## Запуск

```bash
cd ./WorkDocker/docker-compose-test/
docker-compose up -d
```