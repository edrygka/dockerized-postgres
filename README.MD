
## Build postgres in docker

> $ docker run --name docker-postgres -p 5432:5432 -e POSTGRES_PASSWORD=pass -d onjin/alpine-postgres


## Run to connect to postgres 

> $ docker run -it --link docker-postgres:postgres --rm onjin/alpine-postgres sh -c 'exec psql -h "$POSTGRES_PORT_5432_TCP_ADDR" -p "$POSTGRES_PORT_5432_TCP_PORT" -U postgres'

