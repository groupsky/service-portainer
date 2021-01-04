# service-portainer
A docker-compose configuration for portainer service

## Running

1. Clone the repository
    ```shell
    git clone https://github.com/groupsky/service-portainer.git
    cd service-portainer
    ```

2. Configure 
    ```shell
    copy example.env .env
    editor .env
    ```

3. Start
    ```shell
    docker-compose up -d
    docker-compose logs -f
    ```

4. Get the web ui and open in browser
    ```shell
    docker inspect -f 'http://{{.NetworkSettings.Networks.service-portainer_portainer_agent_network.IPAddress}}:9000' service-portainer_portainer_1
    ```

## Using with ingress proxy

The container has configuration for [nginx_proxy](https://hub.docker.com/r/jwilder/nginx-proxy) and [traefik](https://hub.docker.com/_/traefik).
