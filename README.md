# docker-traefik-example

A simple 'how to' to serve http://localhost/whoami behind Traefik.

## Docker compose cheatsheet
* `docker-compose up -d`
* `docker-compose logs -f`
* `docker-compose down`
* `docker-compose rm`

## Troubleshooting

### HTTP
* `wget --no-proxy --header 'Host:localhost' http://localhost/whoami -vv`
* `curl --noproxy '*' -H Host:localhost http://127.0.0.1/whoami -vv`

### Bash
`docker-compose exec reverse-proxy /bin/sh`

