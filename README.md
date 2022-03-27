# docker_elk
Docker composition for ELK (Elasticsearch -- Logstash -- Kibana)

## Install and run
1. Git clone.
```shell
git clone git@github.com:SPTolkachev/docker_elk.git
```

2. Create `docker-compose.yml` from `docker-compose.yml.example`.
```shell
cp docker-compose.yml.example docker-compose.yml
```

3. Create `.env` from `.env.example` and change values.
```shell
~$ cp .env.example .env
~$ nano .env
```

4. Create dirs.
- Create dir `~/data/`:
```shell
~$ mkdir data
~$ sudo chmod 777 data
```

- Create dir `~/data/elasticsearch/`:
```shell
~$ mkdir data/elasticsearch
~$ sudo chmod 777 data/elasticsearch
```

- Create dir `~/logs/`:
```shell
~$ mkdir logs
~$ sudo chmod 777 logs
```

- Create dir `~/logs/elasticsearch/`:
```shell
~$ mkdir logs/elasticsearch
~$ sudo chmod 777 logs/elasticsearch
```

- Create dir `~/logs/logstash/`:
```shell
~$ mkdir logs/logstash
~$ sudo chmod 777 logs/logstash
```

5. Pull docker image.
```shell
~$ docker-compose pull
```

6. Run.
```
~$ docker-compose up -d
```

7. Open `http://localhost:5601` (if `KIBANA_PORT=5601` in `.env`) in your browser.


## Config .env
- `STACK_VERSION` -- ELK stack version
- `ES_PORT` -- elasticsearch port
- `LOGSTASH_PORT` -- logstash port
- `KIBANA_PORT` -- kibana port
- `MEM_LIMIT` -- RAM memory limit for elasticsearch (in bites)
