# Readme

* [full install](https://finestructure.co/blog/2016/5/16/monitoring-with-prometheus-grafana-docker-part-1) and [part2](https://finestructure.co/blog/2016/6/9/monitoring-with-prometheus-grafana-docker-part-2) (june 2016)

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

## Risques

Make it possible for Prometheus to scrape its target, no matter where it is.
Authenticate the target, and Prometheus to the target.
Prevent malicious users from messing with the data in flight.



* [Blog devops/prometheus](https://www.robustperception.io/tag/prometheus/)
* [Forum Grafana](https://community.grafana.com/)
* [Grafana Talk](https://www.brighttalk.com/webcast/14395/252679)