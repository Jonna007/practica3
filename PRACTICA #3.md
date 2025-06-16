
# 📄 Práctica No 3 - Gestión de Bases de Datos con y sin Volúmenes usando Docker y TablePlus

## 1. Título

**Práctica No 3**: Gestión de bases de datos mediante Docker y TablePlus

## 2. Tiempo de duración

Aproximadamente 2 horas.

## 3. Fundamentos

En esta práctica, trabajé con bases de datos PostgreSQL utilizando **Docker** para crear contenedores y **TablePlus** como herramienta gráfica. Aprendí a crear y administrar bases de datos, crear tablas, insertar registros y comprobar la persistencia de los datos con y sin el uso de volúmenes de Docker.

Se utilizó `docker run` para levantar contenedores PostgreSQL, y se realizaron conexiones desde TablePlus usando las credenciales generadas en el contenedor. Se verificó la persistencia de datos después de eliminar contenedores, y se aprendió a crear volúmenes con `docker volume create`.

Entre los comandos utilizados:

- `docker pull postgres`
- `docker run --name postgres-db ...`
- `docker exec -it ... psql -U postgres`
- `\q` para salir de PostgreSQL
- `docker stop`, `docker start`, `docker rm -f`
- `docker volume create` y montaje de volúmenes

## 4. Conocimientos previos

Para desarrollar esta práctica fue importante tener conocimientos sobre:
- PostgreSQL y su sintaxis SQL.
- Uso básico de Docker, contenedores y volúmenes.
- Manejo de TablePlus como herramienta gráfica para conectarse a bases de datos.
- Comandos de terminal.

## 5. Objetivos a alcanzar

- Conectarse a una base de datos PostgreSQL desde TablePlus y Terminal.
- Validar operaciones realizadas desde una herramienta en la otra.
- Entender cómo se comporta una base de datos con y sin persistencia usando volúmenes de Docker.

## 6. Equipo necesario

- **Sistema operativo:** Windows 11 Home
- **Procesador:** AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx 2.10 GHz
- **Memoria RAM:** 8 GB
- **Software:** Docker Desktop, TablePlus, navegador web
- **Conexión a Internet** para documentación y plataforma

## 7. Material de apoyo

- Documentación oficial de Docker
- Manual oficial de PostgreSQL
- Manual de TablePlus
- Videos y guías proporcionados por el docente en la plataforma EVA

## 8. Procedimiento

### Parte 1: Base de datos sin volumen

1. Crear contenedor PostgreSQL `server_db` sin volumen.

2. Conectarse desde TablePlus.
3. Crear base de datos `test` y tabla `customer`.
4. Insertar registros.
5. Detener y eliminar el contenedor.
6. Volver a crear el contenedor `server_db`.
7. Comprobar que los datos no se conservaron (porque no usamos volumen).

### Parte 2: Base de datos con volumen

1. Crear volumen `pg_data` con `docker volume create`.
2. Crear contenedor `server_db2` y montar volumen.
3. Conectarse desde TablePlus.
4. Crear base de datos `test`, tabla `customer`, e insertar datos.
5. Detener y eliminar el contenedor.
6. Volver a crear `server_db2` con el volumen `pg_data`.
7. Comprobar que la base de datos y sus registros **sí persistieron**.

## 9. Resultados esperados

Gracias a esta práctica, comprendí cómo se puede trabajar con PostgreSQL en Docker, y cómo la información se pierde o se conserva según se usen o no volúmenes. TablePlus facilitó la administración de datos y la conexión fue sencilla con las credenciales configuradas.

Con esto, reforcé conocimientos sobre contenedores, persistencia de datos y administración de bases de datos.

## 10. Bibliografía

- Docker Inc. (2024). _Manage data in Docker_ (Volumes). https://docs.docker.com/storage/volumes/
- TablePlus. (2024). _Modern, native tool for relational databases_. https://tableplus.com/
- PostgreSQL Global Development Group. (2023). _PostgreSQL 16 documentation_. https://www.postgresql.org/docs/
