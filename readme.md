# Docker Project: Elasticsearch and Kibana

## Setup

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

## Usage

**Important Note: Before getting started, make sure the latest version of Docker and Docker Compose are installed on your device. Also, be aware of Docker Hub's restrictions regarding US sanctions. Don't forget to use a Virtual Private Network (VPN) if necessary.**

To start the services, use the following command:
```bash
docker compose up
