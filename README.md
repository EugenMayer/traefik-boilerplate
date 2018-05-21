## WAT

Different example traefik configurations for different scenarios for you to start with. 

# Common

i assume you are using docker-for-x so you do not have a docker-machine ip and we suggest localhost - adjust with your ip
if needed.

Traefik Monitoring GUI is always exposed to localhost:8080, http is bound to 80

## File bases

see `docker-compose-file.yml` and start with

```
docker-compose -f docker-compose-file.yml up
```

The configuration is in `traefik/traefik.toml` with then endpoints under `traefik/endpoints`

## Docker based

see `docker-compose-docker.yml` and start with

```
docker-compose -f docker-compose-docker.yml up
```

The configuration is label-based, so check the `docker-compose-docker.yml`

## Consul based

see `docker-compose-consul.yml` and start with

```
docker-compose -f docker-compose-consul.yml up
```

The configuration is should be consul so connect to `localhost:8500`

And start creating backends / frontends like described here https://docs.traefik.io/user-guide/kv-config/#key-value-storage-structure in the `backend 1

