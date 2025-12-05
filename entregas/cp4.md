---
title: Entrega 4 (Final)
parent: Entregas
nav_order: 4
---

# Entrega 4 — Entrega final

## Tareas comprometidas del checkpoint

Para esta entrega se implementó el BackOffice junto con todas sus funcionalidades, y se terminaron de desarrollar y de pulir todas las historias de usuario obligatorias y las optativas elegidas por el equipo. 

- App: Que el reproductor soporte videos musicales

### Setup Melodía Backoffice
- Creación de repositorio → Vite
- Inicialización y estructura de proyecto
- Conexión con Firebase
- Creación de CI-CD
- Setup GitHub Actions
- Conexión y deploy automático en algún Cloud Provider
- Conexión con Melodía Auth
- Endpoint de obtención de todos los datos a partir de un user-auth-id
- AI: Endpoint para todas las métricas a partir de un user-auth-id

### Épica: Administración de usuarios
- Listar usuarios del sistema
- MelodiaBackoffice: Listar usuarios del sistema: Crear pantalla de login
- MelodiaBackoffice: Listar usuarios del sistema: Consultar a MelodiaAuth si el usuario es un Admin, sino no dejarlo entrar al sistema
- MelodiaAuth: Listar usuarios del sistema: Crear endpoint para backoffice, retornando role del usuario
- MelodiaBackoffice: Listar usuarios del sistema: Crear pantalla con listado de usuarios y acciones para cada uno de ellos
- MelodiaBackoffice: Listar usuarios del sistema: Preguntar a MelodiaCore los usuarios del sistema
- MelodiaCore: Listar usuarios del sistema: Crear endpoint para retornar todos los usuarios del sistema (role Admin requerido - `GET /api/admin/users`)
- MelodiaCore: Listar usuarios del sistema: Crear endpoint para eliminar un usuario
- MelodiaAuth: Listar usuarios del sistema: Crear endpoint para eliminar un usuario
- MelodiaAuth: Listar usuarios del sistema: Crear endpoint para cambiar el role de un usuario
- MelodiaAuth: Listar usuarios del sistema: Crear endpoint para bloquear un usuario (y desbloquear)
- MelodiaBackoffice: Listar usuarios del sistema: Si no hay usuarios disponibles mostrar cartel especificando
- Visualizar perfil de usuario
- MelodiaBackoffice: Visualizar perfil de usuario: Crear pantalla de visualización de perfil del usuario
- MelodiaBackoffice: Visualizar perfil de usuario: Consumir endpoint de visualización de usuario específico del core
- MelodiaCore: Visualizar perfil de usuario: Crear endpoint para retornar un usuario específico para el backoffice
- Bloquear usuario
- MelodiaBackoffice: Bloquear usuario: Crear un popup de confirmación antes de bloquear-desbloquear un usuario

### Épica: Onboarding Usuario
- Personalización de Notificaciones Iniciales

### Épica: Administración de contenido
- Catálogo — Explorar y buscar contenido
- BackOffice: crear pantalla Administración → Catálogo con una tabla con Tipo (Canción/Colección), Título, Artista principal, Colección (si es Canción), Fecha de publicación (si aplica), Estado efectivo (Programado / Publicado / No-disponible-región / Bloqueado-admin) y Acciones (Abrir detalle, Editar metadatos, Editar disponibilidad, Bloquear/Desbloquear)
- Core: endpoint que liste las canciones y releases con los datos mencionados y que posea filtros optativos (Tipo, Estado efectivo, Rango de fecha de publicación, Tiene video (sí/no) y Región)
- Core: endpoint que permita bloquear/desbloquear canciones y releases
- Core: endpoint que permita editar metadatos de canciones
- Core: agregar fix para que no se muestren canciones bloqueadas en los endpoints que listan tracks
- BackOffice: buscador para encontrar resultados dentro de la tabla
- Catálogo — Detalle y trazabilidad
- BackOffice: permitir ver el detalle de una canción al clickearla mostrando Resumen, Disponibilidad, Apariciones y Auditoría (ver los CAs para más detalles)
- Core: endpoint que devuelva los detalles de un release requeridos por los CAs (resumen, disponibilidad, apariciones y auditoría)
- Transiciones y estado efectivo del catálogo
- Core: endpoint para obtener releases status (Programado, Publicado, Bloqueado-admin)
- Core: endpoint para obtener track status (bloqueado/no bloqueado) usando el booleano allow_preview

### Épica: Métricas
- Métricas de canciones y álbumes
    - BackOffice: mostrar métricas de canciones y álbumes
    - Melodía-AI: endpoints para devolver métricas de canciones y álbumes
    - BackOffice: pantalla de sección de métricas

- Métricas de usuario
    - BackOffice: pantalla con panel con las métricas clave (usuarios activos, nuevos registros, retención)
    - BackOffice: botón para exportar las métricas en formato CSV o Excel
    - BackOffice: al clickear una métrica específica, ver desglose detallado (demografía, actividad principal)

### Épica: Artista
- App: conectar “Aparece en” con el backend (endpoint GET /artists/{artist_id}/collaborations de Core)
- Deeplink: Consultar si entra
- App: conectar las secciones de Popular Releases y Singles & EPs con el backend:

### Épica: Biblioteca 
- Creación Asistida de ‘Mood Mixes’ (IA) 
    - App: agregar botón de ‘Crear Mood Mix’ -> al apretarlo se le muestra  una selección de canciones
    - AI: endpoint que devuelva una selección de canciones recomendadas en base a historial y me gustas

### Épica: Social
- Compartir Canciones y Playlists
    - deep link
    - Copiar deep link de cancion
    - Copiar deep link de playlist
    - Enviar cancion a contacto directamente
    - Enviar playlist a contacto directamente
    - Agregar canciones a playlists
- Auth: me pidio un endpoint mas
- Fix de silenciar notificaciones

## Resumen de Historias Optativas Realizadas

- Login con proveedor federado
- Ver perfil de otros usuarios
- Enrutamiento al hacer clic en notificaciones
- Visualizar perfil de usuario (admin)
- Métricas de canciones/álbumes
- Colaboraciones / “Aparece en”
- Artistas relacionados (Similares a)
- Explorar Home (base)
- [Home] New release from {Artist}
- Creación Asistida de ‘Mood Mixes’ (IA)
- Videos musicales asociados
- Reproducción continua (autoplay sin cola) [IA]
- Seguimiento de Perfiles de Usuario
- Compartir Canciones y Playlists
- Auto Play (nuevo contexto de 15 canciones) [IA]
- Onboarding: Personalización de Notificaciones


## Estado al finalizar el checkpoint


## Resultados Finales
