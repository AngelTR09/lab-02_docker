# Laboratorio 02
Hoy utlizaremos docker compose para poder desplegar un servicio web y una base de
datos
STACK Tecnico
API
- Aplicación JAVA dockerizarla (crear la imagen)
- docker pull nmatsui/hello-world-api
- clever_montalcini 3001
- condescending_davinci 3000
- $ docker run -d --rm -p 3000:3000 nmatsui/hello-world-api
-
BD PostgreSQL
docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres
COMANDOS
Deben especificar los comandos que voy a ejecutar
```bash
docker compose up -d
```
CONFIGURACIONES
.env
```
VAR=VALUE
```
# Actividad
Trabajar un docker compose, especificando configuración y comandos para despliegue.
Debe permitir lo siguiente:
- 3 copias de una API build local
![Evidencia de cofuncionamiento del docker compose](./evidencias/dockercomposeup-d--build.png)
![Evidencia de cofuncionamiento del docker ps](./evidencias/dockerps.png)
![Evidencia de cofuncionamiento del curl y sus puertos correspondientes](./evidencias/EvidenciaAPI123.png)

- Configuración BD

- Uso de volúmenes
- Uso de variables de entorno
- En README. Responder los tipos de redes y los tipos de volumen que existen en
docker
- Hacer uso de Conventional Commits
- Repositorio publico
- Uso de .gitignore
- Opcional: Capturas de su proyecto desplegado