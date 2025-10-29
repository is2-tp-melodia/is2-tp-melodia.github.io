---
title: Entrega 1
parent: Entregas
nav_order: 1
---

# Entrega 1 — Alcance y avances

Para la primer entrega, separamos las tareas a las que nos comprometimos en "Tareas/Historias implícitas" y "Tareas/Historias explícitas", ya que esta entrega implicó muchas cuestiones operativas y de configuración (crear y configurar los repositorios con todo lo necesario, hostear nuestros servicios y las bases de datos, desplegar coverage, etc).

## Tareas comprometidas del checkpoint

### Tareas/Historias implícitas

**Setup Aplicación React Native**
- Creación de repositorio
- Inicialización y estructura de proyecto
- Conexión con Firebase
- Conexión con Melodía Auth
- Conexión con Melodía Core

**Setup Melodía Auth**
- Creación de repositorio → Node.js + Express
- Inicialización y estructura de proyecto (estructura de carpetas, middlewares, manejo de errores, etc)
- Dockerización del proyecto
- Creación de CI-CD
- Setup Github Actions
- Conexión y migraciones con DB de producción
- Conexión y deploy automático en algún Cloud Provider
- Diseño de Base de Datos y creación de Entidades
- Configurar coverage
- Configuración de DataDog

**Setup Melodía Gateway**
- Creación de repositorio
- Dockerización del proyecto
- Deploy en la nube
- Conexión con Melodía Auth
- Conexión con Melodía Core
- Exposición de endpoint

**Setup Melodía Core**
- Creación de repositorio → FastAPI + …
- Inicialización y estructura de proyecto (estructura de carpetas, middlewares, manejo de errores, etc)
- Dockerización del proyecto
- Creación de CI-CD
- Setup Github Actions
- Conexión y migraciones con DB de producción
- Conexión y deploy automático en algún Cloud Provider
- Diseño de Base de Datos y creación de Entidades
- Conexión con Melodía Auth
- Configurar coverage
- Configuración de DataDog

**Prototipado de pantallas y flujos**
- Prototipado

### Tareas/Historias explícitas

**Épica Usuarios**

- Registro de usuarios
- MelodiaApp: Registro de usuarios: Crear pantalla de registro
- MelodiaApp: Registro de usuarios: Crear usuario en FirebaseAuth
- MelodiaApp: Registro de usuarios: Crear usuario y perfil en MelodiaCore
- MelodiaCore: Registro de usuarios: Crear endpoint de creación de usuario y perfil
- MelodiaCore: Registro de usuarios: Consumir endpoint de creación de usuario en MelodiaAuth
- MelodiaAuth: Registro de usuarios: Crear endpoint de creación de usuario con el role y el proveedor de auth correcto
- Login con email y contraseña
- MelodiaApp: Login con email y contraseña: Crear pantalla de inicio de sesión
- MelodiaApp: Login con email y contraseña: Login contra FirebaseAuth y obtención de accessToken
- MelodiaApp: Login con email y contraseña: Manejo de errores en el inicio de sesión
- MelodiaApp: Login con email y contraseña: Manejo de contexto de sesión iniciada (bloquear todas las rutas si no está la sesión iniciada)
- Login con proveedor federado
- MelodiaApp: Login con proveedor federado: Permitir inicio de sesión con Prov.Federado
- MelodiaApp: Login con proveedor federado: Permitir creación de usuario con Prov.Federado
- MelodiaApp: Login con proveedor federado: Avisar a MelodiaAuth de los inicio de sesión federados para vincular cuentas en caso de corresponder
- MelodiaAuth: Login con proveedor federado: Crear endpoint para vincular una cuenta a un Prov.Federado
- Recuperación de contraseña
- MelodiaApp: Recuperación de contraseña: Agregar botón de olvide mi contraseña
- MelodiaApp: Recuperación de contraseña: Acción de cambio de contraseña
- MelodiaApp: Recuperación de contraseña: Manejo de enlaces expirados

**Épica: Perfil**

- Visualización de perfil propio
- MelodiaApp: Visualización de perfil propio: Crear pantalla de visualización de perfil
- MelodiaCore: Visualización de perfil propio: Crear endpoint para retornar el perfil de un usuario (propio - GET /api/profile/me)
- MelodiaApp: Visualización de perfil propio: Consumir endpoint para obtener los datos de los perfiles
- Edición de perfil
- MelodiaApp: Edición de perfil: Crear pantalla de edición de perfil
- MelodiaApp: Edición de perfil: Consumir endpoint de actualización de perfil en MelodiaCore
- MelodiaCore: Edición de perfil: Crear endpoint para actualizar perfil (también actualizar el mail en MelodiaAuth)
- MelodiaAuth: Edición de perfil: Crear endpoint para actualizar email
- Visualización de perfil de otros usuarios
- MelodiaApp: Visualización de perfil de otros: Crear pantalla de listado de usuarios para acceder a su perfil
- MelodiaApp: Visualización de perfil de otros: Cuando no es mi perfil tiene que estar la posibilidad de seguir/dejar de seguir al usuario
- MelodiaCore: Visualización de perfil de otros: Crear endpoint para retornar el perfil de un usuario (propio - GET /api/profile/<id>), es un endpoint separado porque acá tenemos que consumir la actividad reciente (Me gusta / playlists publicas, lo sigo o no, etc)
- MelodiaCore: Visualización de perfil de otros: Crear endpoint para seguir/dejar de seguir a un usuario (POST /api/profile/<id>/action)

## Estado al finalizar el checkpoint

- Se pudo cumplir con todas las historias comprometidas

## Próximos pasos

- Definir historias comprometidas para E2

