# Evidencias de Base de Datos

Bienvenido al repositorio dedicado a las tareas y evidencias del curso de **Base de Datos**. Aquí encontrarás todo lo necesario para configurar y utilizar el entorno de desarrollo, así como las instrucciones para el manejo de las bases de datos.

## Configuración del Entorno de Desarrollo

Para garantizar un funcionamiento óptimo, sigue detenidamente los siguientes pasos para configurar tu entorno de desarrollo:

### Requisitos Previos

Antes de comenzar, asegúrate de tener instalados:

- [Docker](https://www.docker.com/): Un sistema de contenedores que facilitará la gestión de tus bases de datos.
- [Docker Compose](https://docs.docker.com/compose/): Una herramienta para definir y ejecutar aplicaciones Docker multi-contenedor.

Verifica la instalación de Docker Compose con el siguiente comando:

```shell
docker-compose --version
```

### Configuración de Variables de Entorno

Configurar las variables de entorno es esencial para el correcto funcionamiento del proyecto:

1. Clona este repositorio en tu máquina local.

2. Dentro del repositorio, crea una carpeta llamada `secrets`. Agregar las variables de entorno ubicadas en esta carpeta, ajustándolas a tus necesidades.

2. Dentro del repositorio, crea una carpeta llamada `bd`. Esto para poder perservar los datos de MySql

La estructura de tu proyecto debería verse así:

```
base_datos/
|-bd/
|-secrets/
|-docker-compose.yml
|-README.md
```

### Configuración de Secrets

Es necesario establecer ciertas variables de entorno para la base de datos, las cuales se guardan en archivos dentro de la carpeta `secrets`:

- **MYSQL_ROOT_PASSWORD.txt**: Contiene la contraseña del usuario root de MySQL.
- **MYSQL_DATABASE.txt**: Especifica el nombre de la base de datos principal.
- **MYSQL_USER.txt**: Indica el nombre del usuario de MySQL con acceso a la base de datos.
- **MYSQL_PASSWORD.txt**: Guarda la contraseña del usuario especificado en `MYSQL_USER.txt`.

Asegúrate de llenar estos archivos con la información correspondiente antes de iniciar el entorno con Docker.

## Iniciando el Proyecto

Sigue estos pasos para poner en marcha el proyecto:

1. Abre una terminal y navega al directorio raíz del proyecto.

2. Ejecuta el comando siguiente para construir e iniciar los servicios definidos en tu `docker-compose.yml`:

   ```shell
   docker-compose up
   ```

3. Una vez los servicios estén en ejecución, podrás acceder a phpMyAdmin en la siguiente dirección:

   ```
   http://localhost:8080
   ```

4. Utiliza la contraseña definida en tus `secrets` para ingresar a phpMyAdmin.
