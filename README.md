# Docker-Consul v0.5.0

Docker container for consul

* Basic Command (Agent)

```
docker run -it -p 8400:8400 -p 8500:8500 -p 8600:53/udp oba11/consul
```

* Command As Single-Node Server

```
docker run -it -p 8400:8400 -p 8500:8500 -p 8600:53/udp oba11/consul -server -bootstrap
```

* Using it with Consul Atlas

```
docker run -it -p 8400:8400 -p 8500:8500 -p 8600:53/udp -E ATLAS_TOKEN=my_atlas_token \
  oba11/consul -server -bootstrap -atlas atlas_id/infrastructure_id -atlas-join


docker run -it -p 8400:8400 -p 8500:8500 -p 8600:53/udp oba11/consul \
  -server -bootstrap -atlas atlas_id/infrastructure_id -atlas-join \
  -atlas-token my_atlas_token
```
