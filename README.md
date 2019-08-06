# Docker-based Streaming Architecture

End-to-end streaming architecture (from ingestion to analytics), based on Docker containers.

![Architecture](img/architecture.png)

## Ingestion: Apache NiFi

* Run the NiFi docker container:

```
docker run --name nifi -p 8080:8080 -d apache/nifi:latest
```

* Go to the following URL: http://192.168.99.100:8080/nifi/

**Reference**: https://hub.docker.com/r/apache/nifi/

## Messaging: Apache Kafka

* Go to the kafka folder:

```
cd src/kafka
```

* Run the Docker compose (will launch Zookeeper and a Kafka broker):

```
docker-compose up -d
```
