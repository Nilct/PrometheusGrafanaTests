# Monitoring

## Dépots

* [RobustPerception](https://github.com/RobustPerception)

Exemple java, go, python (bof)

## Monitoring docker host containers

<https://stefanprodan.com/2016/a-monitoring-solution-for-docker-hosts-containers-and-containerized-services/>

> The fact that you can use the same language for graphing and alerting makes the monitoring task a whole lot easier.

> While Grafana supports authentication, the Prometheus and AlertManager services have no such feature. You can remove the ports mapping from the docker-compose file and use NGINX as a reverse proxy providing basic authentication for Prometheus and AlertManager.

Pour tester une alerte :
`docker run --rm -it busybox sh -c "while true; do :; done"`

## Send slack notif

http://opencapacity.co/news/2016/6/6/dev-talk-monitoring-with-prometheus-grafana-docker-part-2

## Showcase

http://play.grafana.org/dashboard/db/grafana-play-home?orgId=1