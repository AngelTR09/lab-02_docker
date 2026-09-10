# Laboratorio 02
Hoy utlizaremos docker compose para poder desplegar un servicio web y una base de datos

# STACK Tecnico
## API
- Aplicación JAVA dockerizarla (crear la imagen)
- docker pull nmatsui/hello-world-api
- clever_montalcini 3001
- condescending_davinci 3000
- $ docker run -d --rm -p 3000:3000 nmatsui/hello-world-api
-
## BD PostgreSQL
docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres
# COMANDOS
Deben especificar los comandos que voy a ejecutar
## Levantar un contenedor
```bash
docker compose up -d
```
## Dar de baja a un contenedor
```bash
docker compose stop db
```
## Dar de baja a todos los contendores
```bash
docker compose down
```

# CONFIGURACIONES
Se necesita crear un .env guiado del .env.example
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

![Levantamiento de la base de datos](./evidencias/dockerc-compose-up-d-db.png)

![Log al subir la base de datos](./evidencias/docker-compose-logs-db.png)

- Uso de volúmenes

![Configuracion del docker compose para los volumenes](./evidencias/evidencia01volumen.png)

![Lista de volumenes](./evidencias/volumen02dockervolumen_ls.png)

![Prueba de persistencia](./evidencias/evidenciaPersistente.png)
- Aqui vemos que aun se mantienen, tras abaje bajado y subido el docker
![Prueba de persistencia](./evidencias/evidenciaPersistente1.png)

- En README. Responder los tipos de redes y los tipos de volumen que existen en docker
    - Redes:
        -
        - bridge: es la configración por defecto. Donde los contenedores estan en el mismo entorno aislado.
        - host: es un contenedor usa la red de la misma computadora.
        - none: contenedor aislado en su totalidad, sin intenet ni a otros contenedores.
        - overlay: conecta contenedores entre varios servidores distintos.
        - macvlan: da al contenedor su propia IP real, haciendolo parecer a un modem.

    - Volúmenes:
        - 
        - Named volumenes: los administra de manera segura y para que las BD no pierda su información.
        - Bind mounts: vincula una carpeta al contenedor.
        - tmpfs mounts: usa  la memoria RAM para guardar diferentes archivos, y al apagar el contenedor todo desaparece.
- Uso de variables de entorno
![Uso correcto del .env.example](./evidencias/evi_variableEntorno1.png)
![Uso correcto del .env.example](./evidencias/evi_variableEntorno.png)
![Uso correcto del .env.example](./evidencias/evi_variableEntorno2.png)

- Hacer uso de Conventional Commits
- Repositorio publico
- Uso de .gitignore
- Opcional: Capturas de su proyecto desplegado