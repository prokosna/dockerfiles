# Kibana Dockerfile

Customized Kibana Docker image.

## Usage

- Build

```
$ docker build -t prokosna_kibana:5.0 ./
```

- Run

```
$ docker run -d --name kibana -p 5601:5601 prokosna_kibana:5.0
```
