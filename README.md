# Docker-based Streaming Architecture

End-to-end streaming architecture (from ingestion to analytics), based on Docker containers.

![Architecture](img/architecture.png)

## Setup

### Pre-requisites

* Download & install Docker: https://docs.docker.com/install/

### Launch the architecture

* Go to the main Docker Compose folder:

```
cd src/main
```

* Run the Docker compose:

```
docker-compose up -d
```

## Component list

The list of components and it Docker name is the following:

| Service | Hostname | Port | URL (when applies) |
| --- | --- | --- | --- |
| Apache NiFi | nifi | 8080 | http://192.168.99.100:8080/nifi/ |
| Apache Kafka (broker) | kakfa | 9092 | .. |
| Apache Kafka (zookeeper) | zookeeper | 2181 | .. |

## Reference

**Reference**: https://hub.docker.com/r/apache/nifi/
**Reference**: https://hub.docker.com/r/bitnami/kafka/

## Maintenance

Starting and stopping things.

## Troubleshooting

### Adding more memory for the containers

* Using the Docker configuration (when native)
* Manually, using command line
```
docker-machine stop
VBoxManage modifyvm default --cpus 2
VBoxManage modifyvm default --memory 4096
docker-machine start
```

More info: https://stackoverflow.com/questions/32834082/how-to-increase-docker-machine-memory-mac 
