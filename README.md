# data-pipeline-poc
This is a docker compose yml which wraps confluent data platform and memsql

## Quick Start

Install docker tool box for mac or windows if you haven't already. (https://www.docker.com/products/docker-toolbox)
    
    1. Once you have the file downloaded, open and replace KAFKA_ADVERTISED_HOST_NAME: "{SET DOCKER HOST IP}" with the IP of the docker host. Example: KAFKA_ADVERTISED_HOST_NAME: "10.10.0.21". This will ensure Kafka is reachable from any client library.
    2. Run "docker-compose -f data-pipeline-poc.yml up" to start all services
    3. Run "docker-compose -f data-pipeline-poc.yml down" to shut down and dispose all services.
    
## What this docker compose file does.
    1. Creates a bridge network to enable all services define in the file to communicate with each other.
    2. Downloads the latest docker images if it hasn't already and then run each service in their respective containers.
    
## Visit the following for addition information on customizing individual services.
  1. https://github.com/confluentinc/docker-images
  2. https://github.com/memsql/memsql-docker-quickstart
