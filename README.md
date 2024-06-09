# dblab
a linux/docker research env.

1. ubuntu version 24.04
        download ISO file, then make USB drive. Boot from USB then following screen instructions
2. docker
  - https://snapcraft.io/docker
  - ```sudo snap install docker```
  - add user to docker group
3. ollama
  - https://github.com/ollama/ollama
  - can be installed by single line of docker command, or compose
  - default port， **11434**, docker network only (not expose to external)
  - can use API to do LLM applications
4. open webui
  - chatgpt alike chatting client
  - can be installed by docker or composer
  - doc: https://docs.openwebui.com/
  - default port: **8080**
5. docker-compose
  - to run multiple services, which is defined in docker-compose.yml
  - run docker-compose command in yml directory, e.g.
    ```shell
      docker-compose up -d
      docker-compose down
      docker-compose logs -f
      docker-compose ps -a
      docker-compose exec -it ollama /bin/bash
    ```
6. traefik
 - as a reverse proxy, mostly for user apps
 - listen on all **80/443** traffics and then forward to docker services
 - check out http://localhost/whoami as an example (_defined in docker-compose.yml_). 
7. MySQL
 - as docker
 - port 3306

