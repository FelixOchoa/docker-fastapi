# Aplicación FastAPI en Docker

Este proyecto es una aplicación FastAPI que se ejecuta dentro de un contenedor Docker. A continuación, se detallan los pasos para construir y ejecutar la imagen Docker.

## Requisitos

- Docker instalado en tu máquina.
- Archivo `requirements.txt` con las dependencias de Python necesarias.

## Construir la imagen Docker

Para construir la imagen Docker, ejecuta el siguiente comando en la raíz del proyecto (donde se encuentra el `Dockerfile`):

```bash
docker build -t nombre-de-tu-imagen .
```

En este caso usé fastapi-felix entonces sería:

```bash
docker build -t dafedev/fastapi-felix .
```

![Evidencia de creación de la imagen](https://i.imgur.com/VSz7cI1.png)

## Ejecución de contenedor

Para ejecutar el contenedor ejecutas el siguiente comando, el cual creará un contenedor con el nombre de imagen creado previamente y utilizará el puerto que se estableció para el contenedor y otro en el cual podrás acceder desde tu maquina.

```bash
docker run -d -p 8080:8080 --name nombre-de-tu-contenedor nombre-de-tu-imagen
```

En mi caso:

```bash
docker run -d -p 8000:8000 --name fastapi-container dafedev/fastapi-felix
```

Luego visualizas en tu navegador la URL y ya puedes acceder al resultado:
