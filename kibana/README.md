# Kibana Dockerfile

Customized Kibana Docker image.

## Usage

- Build

```
$ docker build -t prokosna_kibana:4.6 ./
```

- Run

```
$ docker run -d --name kibana --restart=on-failure:5 -p 5601:5601 prokosna_kibana:4.6
```
