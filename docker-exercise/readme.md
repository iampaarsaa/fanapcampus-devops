# Docker Project: Elasticsearch and Kibana
## Usage

To allocate enough virtual memory, use the following command:
```bash
sudo sysctl -w vm.max_map_count=262144
```

To start the services, use the following command:
```bash
docker compose up -d
```
## More Details:

The project uses Docker Compose to define and run the multi-container Docker applications. The `docker-compose.yml` file is used to define the services, networks, and volumes.

### Services

Two services are defined: `Elasticsearch` and `Kibana`.

### Networks

A network named `elk_network` is created with a driver of `bridge` and a subnet range defined in the `.env` file.

### Volumes

Two volumes are created: `elasticsearch_data` and `kibana_data`, both with a local driver.

## Ports

The Elasticsearch service is exposed on port 9200 and Kibana on port 5601.

## Healthcheck

A healthcheck is defined for the Elasticsearch service to check the health of the container every 30 seconds.

## Environment Variables

Environment variables are defined in the `.env` file. These include the stack version, ports for Elasticsearch and Kibana, healthcheck interval, volume driver, network driver, and subnet range.


