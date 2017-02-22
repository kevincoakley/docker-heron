# docker-heron

[![Build Status](https://travis-ci.org/kevincoakley/docker-heron.svg?branch=master)](https://travis-ci.org/kevincoakley/docker-heron)

Heron - A realtime, distributed, fault-tolerant stream processing engine from Twitter - [https://twitter.github.io/heron/](https://twitter.github.io/heron/)


### Start the container:

    docker run --name my_heron -d -p 8888:8888 -p 8889:8889 -v ~/herondata:/root/.herondata -v ~/dev/:/root/dev kevincoakley/heron

### Submit a topology:

    docker exec my_heron heron submit local /root/dev/heron-topo.jar com.twitter.heron.ExampleTopology ExampleTopology --deploy-deactivated

### Activate a topology:

    docker exec -it my_heron heron activate local ExampleTopology

### Kill a topology:

    docker exec -it my_heron heron kill local ExampleTopology

### Get a shell on the container:

    docker exec -it my_heron /bin/bash

### Heron UI:

[http://127.0.0.1:8889/](http://127.0.0.1:8889/)
