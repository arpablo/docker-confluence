# docker-confluence
This image contains
* Postgresql
* Oracle Java 8
* Atlassian Confluence

# How to use this image

## Start image using docker command 
```console
$ docker run --name docker-confluence -d -p 8090:8090 -p 8091:8091 -p 5432:5432 -v ~/docker-confluence/confluence:/var/confluence -v ~/docker-confluence/postgres:/var/lib/postgresql/data arpablo/docker-confluence
```

## Start image using docker-compose
```console
$ docker-compose -f docker-confluence.yml
```

The provided example docker-confluence.yml

```console
version: '2'
services:
  confluence:
    image: arpablo/docker_confluence
    
    ports:
      - 5432:5432
      - 8090:8090
      - 8091:8091
    volumes:
      - ~/docker-confluence/confluence:/var/confluence
      - ~/docker-confluence/postgres:/var/lib/postgresql/data

```



