# global-terrorism-prediction

This project contains a basic docker-compose jupyter notebook data science stack. The goal of this project is to predict and classify terrorism incidents using the [Global Terrorism DB of worldwide terrorism incidents since 1970](https://www.kaggle.com/ecodan/global-terrorism-db).

## Run the stack

- Run with output
```
$ docker-compose up
```

- Run without output
```
$ docker-compose up -d
```

- Follow the output when the stack runs in daemon (-d)
```
$ docker-compose logs -f | grep -v jupyter_1
```

- Open a window in your favorite browser and got to localhost:8888

## Docker compose

### Install and release

[Install](https://docs.docker.com/compose/install/)

[Release](https://github.com/docker/compose/releases)

### Working with containers and images

- Open container
```
$ docker exec -ti [container name(ex: bd04...)] /bin/bash
```

- Remove all containers and images
```
#!/bin/bash
# Delete all containers
$ docker rm $(docker ps -a -q)
# Delete all images
4 docker rmi $(docker images -q)
# Maintenant la commande purge existe:
$ docker [image|container|volume|network|system] purge
```

- List stopped containers
```
docker ps -q --filter "status=exited"
```

- Remove stopped containers
```
docker rm $(docker ps -q --filter "status=exited")
```

- Clean up any resources — images, containers, volumes, and networks — that are dangling (not associated with a container)
```
docker system prune
```

- Remove dangling volumes:
[Remove dangling volumes](https://stackoverflow.com/questions/27812807/orphaned-docker-mounted-host-volumes)

- List all orphaned volumes and Eliminate all of them
```
$ docker volume ls -qf dangling=true
$ docker volume rm $(docker volume ls -qf dangling=true)
```

- Alias to have the container name in stats
```
alias ds='docker stats --format "table {{.Name}}\t{{.Container}}\t{{.CPUPerc}}\t{{.MemUsage}}\t{{.NetIO}}\t{{.BlockIO}}\t{{.MemPerc}}\t{{.PIDs}}"'
```

### Docker

- [Pass environment variables to containers](https://docs.docker.com/compose/environment-variables/#pass-environment-variables-to-containers)

- [Dockerfile best practices](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/)

- [10 tips for docker-compose with multiple dockerfiles](https://nickjanetakis.com/blog/docker-tip-10-project-structure-with-multiple-dockerfiles-and-docker-compose)

- [Multiple dockerfiles in project](https://stackoverflow.com/questions/27409761/multiple-dockerfiles-in-project)

- [Docker ELK stack for devops](https://medium.com/tech-tajawal/elk-stack-docker-playground-for-devops-221179ca00dd)

## Articles

- [Global Terrorism DB](https://www.kaggle.com/ecodan/global-terrorism-db)
