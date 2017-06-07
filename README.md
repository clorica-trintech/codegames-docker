# ELK (Elasticsearch, Logstash, Kibana) 5.4.0 stack on Docker

Pulls and runs the official images:
* [elasticsearch](https://github.com/elastic/elasticsearch-docker)
* [logstash](https://github.com/elastic/logstash-docker)
* [kibana](https://github.com/elastic/kibana-docker)

## Setup

1. Download and Install [Docker Community Edition](https://download.docker.com/win/stable/InstallDocker.msi)
2. Download [Kitematic](https://download.docker.com/kitematic/Kitematic-Windows.zip) and unzip to the Docker installation folder (e.g. C:\Program Files\Docker\Kitematic)
3. Right click Docker icon -> Settings ... 
    -> Share -> Shared Drives -> Share Drives C: and E:
    -> Advanced -> Increase memory to at least 4G
4. Add the [Sense Chrome Extension](https://chrome.google.com/webstore/detail/sense-beta/lhjgkmllcaadmopgmanpapmpjgmfcfig?hl=en)  to your browser 
5. On the command line, go to the directory where you extracted this folder and run docker compose
    ```
    E:\Projects\workspace\CodeGamesDocker> docker-compose up
    ```
    
## Usage

### HTTP
You can access ElasticSearch and Kibana by hitting the following URLs:
- ElasticSearch: [http://localhost:9200](http://localhost:9200)
- Kibana: [http://localhost:5601](http://localhost:5601)

Ports:
- Logstash
    - TCP: 5000
- ElasticSearch
    - HTTP: 9200
    - TCP: 9300
- Kibana
    - HTTP: 5601

### Sense
Open the Chrome extension and run any RESTful command on ElasticSearch (Server: localhost:9200)
e.g.
```
    POST close/_search
    {
       "query": {
          "match_all": {}
       }
    }
```

