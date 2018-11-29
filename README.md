# GRADIANT JUPYTER NOTEBOOK EXAMPLE COLLECTION

## Quick Start

Just run a [gradiant/jupyter:5.70-spark2.4.0](https://hub.docker.com/r/gradiant/jupyter/) container pointing to this github repo:

```
docker run -p 8888:8888 -ti --rm -e NOTEBOOKS_URL=https://github.com/Gradiant/notebooks.git --name=jupyter -h jupyter gradiant/jupyter:5.7.0-spark2.4.0
```

Explore notebooks at [http://localhost:8888](http://localhost:8888)

Spark UI links can work if you add a entry in /etc/hosts for your jupyter container hostname. The entry can be obtained with this command:

```
docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}} {{.Config.Hostname}}' jupyter
```

