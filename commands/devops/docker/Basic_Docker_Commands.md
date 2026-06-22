# 🐳 Comandos Docker Básicos

| Descripción | Comando |
|--------------|----------|
| Versión de Docker instalada | ```docker --version``` |
| Información del sistema Docker | ```docker info``` |
| Ayuda general o de un comando específico | ```docker help``` |
| Descargar una imagen desde Docker Hub | ```docker pull <imagen>``` |
| Listar todas las imágenes descargadas | ```docker images``` |
| Eliminar una imagen | ```docker rmi <imagen>``` |
| Construir una imagen desde un Dockerfile | ```docker build -t <nombre> .``` |
| Renombrar o etiquetar una imagen | ```docker tag <imagen> <nombre:tag>``` |
| Ejecutar un contenedor a partir de una imagen | ```docker run <imagen>``` |
| Ejecutar un contenedor en segundo plano | ```docker run -d <imagen>``` |
| Ejecutar un contenedor con terminal interactiva | ```docker run -it <imagen> /bin/bash``` |
| Listar contenedores en ejecución | ```docker ps``` |
| Listar todos los contenedores (incluso detenidos) | ```docker ps -a``` |
| Detener un contenedor | ```docker stop <id>``` |
| Iniciar un contenedor detenido | ```docker start <id>``` |
| Reiniciar un contenedor | ```docker restart <id>``` |
| Eliminar un contenedor detenido | ```docker rm <id>``` |
| Ver logs de un contenedor | ```docker logs <id>``` |
| Entrar dentro de un contenedor en ejecución | ```docker exec -it <id> /bin/bash``` |
| Mostrar información detallada de un contenedor | ```docker inspect <id>``` |
| Eliminar contenedores, redes e imágenes no usadas | ```docker system prune``` |
| Eliminar solo los contenedores detenidos | ```docker container prune``` |
| Eliminar solo las imágenes sin uso | ```docker image prune``` |
| Eliminar volúmenes no usados | ```docker volume prune``` |
| Listar redes existentes | ```docker network ls``` |
| Crear una nueva red | ```docker network create <nombre>``` |
| Mostrar detalles de una red | ```docker network inspect <nombre>``` |
| Eliminar una red | ```docker network rm <nombre>``` |
| Listar volúmenes existentes | ```docker volume ls``` |
| Crear un volumen | ```docker volume create <nombre>``` |
| Mostrar información de un volumen | ```docker volume inspect <nombre>``` |
| Eliminar un volumen | ```docker volume rm <nombre>``` |
| Levantar servicios definidos en docker-compose.yml | ```docker compose up``` |
| Levantar los servicios en segundo plano | ```docker compose up -d``` |
| contruir el docker ya creado isn danar lo que esta corriendo| ```docker compose up -d --build``` |
| Detener y eliminar los servicios del compose | ```docker compose down``` |
| Listar servicios activos del compose | ```docker compose ps``` |
| Ver logs en tiempo real de todos los servicios | ```docker compose logs -f``` |
| Detener todos los contenedores activos | ```docker container stop $(docker ps -q)``` |
| Eliminar todos los contenedores | ```docker container rm $(docker ps -aq)``` |
