# Readme

* [full install](https://finestructure.co/blog/2016/5/16/monitoring-with-prometheus-grafana-docker-part-1) and [part2](https://finestructure.co/blog/2016/6/9/monitoring-with-prometheus-grafana-docker-part-2) (june 2016)

Extract:

* **Prometheus** - this is the central piece, it contains the time series database and the logic of scraping stats from exporters (see below) as well as alerts.
* **Grafana** is the ‘face’ of Prometheus. While Prometheus exposes some of its internals like settings and the stats it gathers via basic web front-ends, it delegates the heavy lifting of proper graphical displays and dashboards to Grafana.
* **Alertmanager** manages the routing of alerts which Prometheus raises to various different channels like email, pagers, slack - and so on. So while Prometheus collects stats and raises alerts it is completely agnostic of where these alerts should be displayed. This is where the alertmanager picks up.
* **Exporters** are http endpoints which expose ‘prometheus metrics’ for scraping by the Prometheus server. What this means is that this is a pull set-up. Note that it is also possible to set up a push-gateway which is essentially an intermediary push target which Prometheus can then scrape. This is useful for scenarios where pull is not appropriate or feasible (for example short lived processes).

A voir (influxDB): [TICK](https://www.influxdata.com/products/open-source/)

## Extensions

* [client libs](https://prometheus.io/docs/instrumenting/clientlibs/) : go, java/scala, python (officiel), erlang


## Culture

* Push vs pull service discovery (Prometheus is pull-based)

## Limites / choix

From <https://stefanprodan.com/2016/a-monitoring-solution-for-docker-hosts-containers-and-containerized-services/>

> The fact that you can use the same language for graphing and alerting makes the monitoring task a whole lot easier.

> While Grafana supports authentication, the Prometheus and AlertManager services have no such feature. You can remove the ports mapping from the docker-compose file and use NGINX as a reverse proxy providing basic authentication for Prometheus and AlertManager.

> Also Docker (v1.13) and Kubernetes have builtin integration with Prometheus, so it's the obvious choice if you are using these technologies.

?? https://github.com/stefanprodan/goc-proxy