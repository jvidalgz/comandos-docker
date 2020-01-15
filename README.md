# comandos-docker
Resumen de comandos cliente docker

Listar todos los containers terminados
docker ps -aq -f status=exited

Eliminar todos los contenedores detenidos
docker ps -aq --no-trunc -f status=exited | xargs docker rm

Eliminar todas las imagenes dangling/untagged
docker images -q --filter dangling=true | xargs docker rmi


Eliminar todos los contenedores creados despues de un contenedor en específico
docker ps --since a1bz3768ez7g -q | xargs docker rm

Mostra os containers em execução:
`docker container ls` 

Mostra todos os containers, em execução, mortos, parados:
`docker container ls -a`

Parar container:
`docker container stop angry_babbage`

Mostra o uso de recursos consumidos pelo container:
`docker container stats 18a58c41ebd1`
