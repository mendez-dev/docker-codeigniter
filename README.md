
# Configuración Docker para Proyecto CodeIgniter

Este repositorio contiene la configuración de Docker para ejecutar un proyecto basado en CodeIgniter con un servidor Apache, una base de datos MariaDB y phpMyAdmin.

## Estructura de Directorios

- `docker/`: Carpeta que contiene la configuración de Docker.
  - `apache/`: Configuración para el servidor Apache.
  - `mariadb/`: Configuración para la base de datos MariaDB.
  - `phpmyadmin/`: Configuración para phpMyAdmin.
  - `docker-compose.yml`: Archivo de composición de Docker para orquestar los contenedores.

## Requisitos

- Docker y Docker Compose instalados en tu sistema.

## Instrucciones de Uso

1. Clona este repositorio en tu máquina local.

   ```bash
   git clone <URL_DEL_REPO>
   ```

2. Dentro de la carpeta `docker`, copia el archivo  `env` y renombralo como `.env` y configura las variables de entorno necesarias, como contraseñas y configuraciones específicas de tu proyecto.

3. Desde la raíz del proyecto, ejecuta el siguiente comando para construir las imágenes de Docker:

   ```bash
   docker-compose build
   ```

4. Una vez que las imágenes se hayan construido, inicia los contenedores con:

   ```bash
   docker-compose up -d
   ```

5. Accede a tu aplicación CodeIgniter en el navegador web en `http://localhost`, a phpMyAdmin en `http://localhost:8080`, y conecta a la base de datos MariaDB con las credenciales configuradas en tu archivo `.env`.

## Personalización

- Puedes personalizar la configuración de Apache y MariaDB según las necesidades de tu proyecto editando los archivos en las carpetas `docker/apache` y `docker/mariadb`, respectivamente.

- Asegúrate de seguir las prácticas de seguridad recomendadas para entornos de producción.

## Licencia

Este proyecto se distribuye bajo la licencia [LICENSE_NAME](LICENSE_URL). Consulta el archivo LICENSE para obtener más detalles.
