# Elasticsearch Dockerfile

I customized official Docker image of Elasticsearch a little bit.

## Usage

- Build

```
$ docker build -t prokosna_elasticsearch:2.4 ./
```

- Data Volume Container

```
$ docker create -v /usr/share/elasticsearch/data --name es_store prokosna_elasticsearch:2.4 /bin/true
```

- Run

```
$ docker run -d --name es_noden --restart=on-failure:5 -p 9200:9200 -p 9300:9300 --volumes-from es_store -e "CLUSTER_NAME=cluster_name" -e "NODE_NAME=noden" -e "MASTER_NUM=N/2+1" prokosna_elasticsearch:2.4
```
