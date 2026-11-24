---
layout: Mi post
title: "Repaso de comandos Git y Docker"
---

# Repaso de comandos Git y Docker

En esta entrada vamos a hacer un repaso de algunos de los comandos más utilizados de **Git** y **Docker**, herramientas que nos permiten gestionar versiones de proyectos, compartir código y trabajar con contenedores.

---

## 1. Git

Git es un sistema de control de versiones que permite registrar los cambios realizados en un proyecto, recuperar versiones anteriores y trabajar con repositorios remotos, como GitHub.

### Inicializar un repositorio

```bash
git init
```

Inicializa un repositorio Git en el directorio actual.

### Comprobar el estado

```bash
git status
```

Muestra los archivos modificados, nuevos archivos y cambios pendientes de guardar en el repositorio.

### Añadir archivos

```bash
git add archivo
```

Añade un archivo concreto a la zona de preparación (staging).

Para añadir todos los archivos modificados:

```bash
git add .
```

### Guardar cambios (commit)

```bash
git commit -m "Descripción de los cambios"
```

Guarda los cambios preparados en el repositorio con un mensaje que describe lo realizado.

### Consultar el historial

```bash
git log
```

Muestra el historial de commits realizados.

Para mostrarlo de forma resumida:

```bash
git log --oneline
```

### Clonar un repositorio

```bash
git clone URL
```

Crea una copia local de un repositorio remoto.

### Subir cambios a GitHub

```bash
git push
```

Envía los commits locales al repositorio remoto.

### Descargar cambios del repositorio remoto

```bash
git pull
```

Descarga e integra los cambios existentes en el repositorio remoto.

---

## 2. Docker

Docker permite crear y ejecutar contenedores, que contienen las aplicaciones y los elementos necesarios para ejecutarlas de forma aislada.

### Descargar una imagen

```bash
docker pull nginx
```

Descarga la imagen de Nginx desde un repositorio de imágenes.

### Listar imágenes descargadas

```bash
docker images
```

Muestra las imágenes que tenemos almacenadas localmente.

### Crear y ejecutar un contenedor

```bash
docker run -d --name web nginx
```

Crea un contenedor llamado `web` a partir de la imagen Nginx y lo ejecuta en segundo plano.

### Listar contenedores en ejecución

```bash
docker ps
```

Muestra los contenedores que están funcionando actualmente.

### Listar todos los contenedores

```bash
docker ps -a
```

Muestra todos los contenedores, incluidos los detenidos.

### Detener un contenedor

```bash
docker stop web
```

Detiene el contenedor llamado `web`.

### Iniciar un contenedor detenido

```bash
docker start web
```

Vuelve a iniciar un contenedor que ya existe y está detenido.

### Eliminar un contenedor

```bash
docker rm web
```

Elimina un contenedor que esté detenido.

### Eliminar una imagen

```bash
docker rmi nginx
```

Elimina una imagen de Docker que no esté siendo utilizada por contenedores existentes.

### Acceder al interior de un contenedor

```bash
docker exec -it web bash
```

Permite ejecutar una terminal interactiva dentro de un contenedor en funcionamiento.

---

## 3. Docker Compose

Docker Compose permite definir y gestionar varios servicios y contenedores mediante un archivo YAML, facilitando su configuración y puesta en marcha.

### Levantar los servicios

```bash
docker compose up -d
```

Crea y arranca los servicios definidos en el archivo `docker-compose.yml` en segundo plano.

### Detener los servicios

```bash
docker compose stop
```

Detiene los servicios sin eliminarlos.

### Detener y eliminar los contenedores

```bash
docker compose down
```

Detiene y elimina los contenedores creados por Compose.

### Consultar los servicios en ejecución

```bash
docker compose ps
```

Muestra el estado de los servicios del proyecto.

### Consultar los logs

```bash
docker compose logs
```

Muestra los registros de los servicios para comprobar su funcionamiento o localizar errores.

---

## Conclusión

Git nos permite mantener un control sobre los cambios que realizamos en nuestros proyectos y compartirlos a través de plataformas como GitHub.

Por otro lado, Docker facilita la creación y gestión de contenedores, mientras que Docker Compose permite administrar varios servicios de forma conjunta mediante un archivo de configuración.

Ambas herramientas son muy útiles en el ámbito de la administración de sistemas y permiten trabajar de forma más organizada y eficiente.
