# Notes

## Various ramblings

* [scaling](https://www.robustperception.io/scaling-and-federating-prometheus/)
* automatic service discovery

!!! **Il faut passer par un dockerfile pour prometheus.yml** <-- à priori non ?

## Install

* [doc](https://prometheus.io/docs/introduction/install/)
* [git](https://github.com/prometheus)
* [docker images](https://hub.docker.com/r/prom/)

### Docker

Basic : `docker run -p 9090:9090 prom/prometheus`

Bind-mount your prometheus.yml from the host + use an additional volume for the config:

``` sh
$ docker-compose rm
$ docker-compose up -d
# check on http://localhost:9090/status (prometheus) and http://localhost:3000/ (grafana)
```

