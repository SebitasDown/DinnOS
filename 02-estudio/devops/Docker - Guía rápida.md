# Docker - Guía Rápida

#estudio #devops #docker

## ¿Qué es?
Docker permite empaquetar aplicaciones en **contenedores**: entornos aislados con todo lo necesario para ejecutarse (código, dependencias, configuración).

## Comandos esenciales

| Comando                                         | Descripción                  |
| ----------------------------------------------- | ---------------------------- |
| `docker ps`                                     | Ver contenedores corriendo   |
| `docker logs <nombre>`                          | Ver logs de un contenedor    |
| `docker stop <nombre>`                          | Detener un contenedor        |
| `docker rm <nombre>`                            | Eliminar un contenedor       |
| `docker run -d --name mi-app -p 8080:80 imagen` | Crear y correr un contenedor |


## Volúmenes
Permiten que los datos persistan aunque el contenedor se elimine:
```bash
docker run -v ~/mis-datos:/app/data mi-imagen
```

## Docker Compose
Permite definir multi-contenedor en un archivo `docker-compose.yml`:
```yaml
services:
  db:
    image: postgres:16
    ports:
      - "5432:5432"
  app:
    build: .
    ports:
      - "3000:3000"
```

## Lo uso en
- [[Backend]] → Mis microservicios corren en Docker
- N8N → Lo tengo corriendo en un contenedor Docker
