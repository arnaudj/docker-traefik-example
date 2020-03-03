# docker-traefik-example

A simple 'how to' to serve http://localhost/whoami behind Traefik.

## Docker compose cheatsheet
* Compose up:
  * `docker-compose up -d`
  * Scale service whoami to 3: `docker-compose.exe up -d --scale whoami=3`
* `docker-compose logs -f`
* Stop: `docker-compose stop`
* Stop+remove: `docker-compose down`

## Troubleshooting

### Direct access to containers
Ensure whoami's `ports` is uncommented in the compose file. Then run `docker-compose ps` to view the ports.

### HTTP
* `wget --no-proxy --header 'Host:localhost' http://localhost/whoami -vv`
* `curl --noproxy '*' -H Host:localhost http://127.0.0.1/whoami -vv`

### Bash
`docker-compose exec reverse-proxy /bin/sh`

