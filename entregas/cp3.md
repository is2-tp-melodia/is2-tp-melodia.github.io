---
title: Entrega 3
parent: Entregas
nav_order: 3
---

# Entrega 3 — Alcance y avances

## Tareas comprometidas del checkpoint

Para esta entrega se terminaron de completar y pulir algunas cuestiones que habían quedado pendientes de la entrega anterior sobre las épicas de Reproducción y Artista, y se implementaron las épicas de Explorar, Biblioteca y Notificaciones.

### Épica: Reproducción
- App: Siguiente o anterior en la cola de reproducción
- App: Mejorar visualización de "agregar canciones a cola de reproducción"
- App: Modo aleatorio
- App: Modo repetir las canciones
- App: Mover orden de las canciones en la cola de reproducción — VICKY
- App: Eliminar canciones de la cola de reproducción (verificar que esté listo)
- App: Borrar todas las canciones de la cola de reproducción
- App: Conectar con backend: conseguir recomendación de canción siguiente
- AI: Darme canción recomendada siguiente — Cami
- App: Usar funcionalidad de obtener próxima canción recomendada
- App: Cada vez que se reproduce una canción, avisarle a Melodia AI
- AI: Endpoint para informar canción reproducida — Vicky
- AI: Endpoint que indique todas las canciones likeadas — Vicky
- App: Poder dar like desde el reproductor
- App: Desde mi perfil -> Biblioteca -> visualización de canciones likeadas
- App: Reproductor soporte videos musicales (opcional: opción para ver video, si no, solo audio) — FACU
- App: Agregar un label al componente de canción indicando que el video está disponible — FACU

### Épica: Artista
- AI: Exponer datos de metricas de artistas: Vicky
- App: Consumir y mostrar las metricas de reproducciones de un artista
- App: Vista para ver todos los seguidores de un artista y que se navegue al perfil de cada seguidor : FACU
- App: Desde el perfil de los artistas tiene que haber un boton que sea play del artista y que se cargue toda la discografia a la lista de reproduccion. Lo mismo con un botón que inice aletoreamente a reproducir todas las canciones de un artista: FACU
- App: El layout de la vista de un artista tiene que ser: Popular → Liked Songs -> Artist Pick -> Discography → → About -> Appears On → Similar Artists : FACU
- App: Mostrar en el perfil del artista la canciones a las que le dio like : FACU
- App: Mostrar en el perfil del artista las canciones mas populares : FACU
- AI: Disponibilidad endpoint para obtener las canciones likeadas de y populares: Vicky
- IA: disponibilizar un endpoint que me de todas las canciones para mostrar en el perfil del artista apenas lo abro [populares, likeadas, etc] (cada categoria dentro de un objeto): Vicky
- App: Consumir melodía AI para mostrar las canciones en el perfil del artista : FACU
- App: Mostrar pestaña de discografia dentro de cada artista (hay requerimientos especiales para esto): FACU
- App: Modificar componente de release para que cumpla con la historia del usuario
- App: Mostrar fecha, hora y cuenta regresiva de los upcoming releases
- App: Agregar pestaña colaboraciones y conectar con el backend : FACU
- Core: Disponibilizar un endpoint de colaboraciones para un artista dado
- IA: Disponibilizar endpoint para obtener los populares de un artista: Vicky
- App: Agregar pestaña populares y mostrar su resultado (pedirlo desde melodia AI): FACU
- App: Agregar botón para reproducir las canciones populares del artista : FACU
- Core: Proveer datos de artistas similares
- App: Agregar pestaña y conectar artistas similares-relacionados : FACU
- App: perfil del artista tiene que mostrar la bio, redes sociales, y toda la metadata disponible: FACU
- App: Agregar boton al perfil del artista, que te lleva al perfil usuario de dicho artista (Al editar no(?)) : FACU
- App: agregar dentro del perfil usuario la lista de canciones likeadas: FACU
- App: Edición del Carrusel de imágenes: FACU
- App: Edición de datos de un release

### Épica: Explorar
- IA: Endpoint que devuelva las recomendaciones para mostrar en la home: Cami
- App: Consumir endpoint del melodia AI para mostrar  en la home :  FACU
- Melodia AI: Disponibilizar endpoint que devuelva mis 8 canciones mas escuchadas, no incluir las likeadas
- App: Armar sección de Mis Atajos en la home (consumir endpoint de canciones likeadas y endpoint de mis canciones mas escuchadas) :  Cami
- Core: Endpoint que devuelva album de artista que estoy siguiendo y esta por sacar musica
- App: Mostrar en la home seccion de proximo release de artista (consumir endpoint de melodia core):  CAMI
- AI: disponibilizar endpoint para preguntar por mis últimas canciones escuchadas
- App: Mostrar en la home seccion de ultimas canciones escuchadas (consumir de melodia AI):  CAMI Y FACU
- App: seccion de Discover more from artist en la home (esto es elegir un artista al azar de los artistas que estoy siguiendo y mostrar mas de su catalogo)
- AI: Disponibilizar endpoint “Made For You”, ver CA para mas informacion
- App: Consumir y mostrar en la home el Made For You
- App: En pantalla de busqueda, hacer que cuando me muevo de pestaña el contenido si filtra segun la opcion seleccionada:FACU
- Core: que el endpoint de busqueda busque perfil por nombre y apellido, artista por nombre artistico, playlist publicas por nombre, nombre de release y canciones: Vicky

### Épica: Biblioteca
- App: En pantalla de mi perfil de usuario, tengo que tener una sección para ver mis playlists: CAMI
- App: hacer pantalla de detalle de playlist :CAMI
- Core: disponibilizar endpoint para crear playlist
- Core: Disponibilizar endpoint para agregar/borrar canciones a las playlist
- Core: Disponibilizar endpoint para que una playlist sea publico
- Core: Disponibilizar endpoint para borrar una playlist
- App: Implementar interacciones con las playlist
- App: Que el componente de cancion permita agregarla a una playlist:FACU
- Core: Disponibilizar endpoint para mostrar todas la playlist de un usuario
- Core: Disponibilizar endpoint para cambiar el orden de las canciones de una playlist
- App: Agregar funcionalidad para reordenar canciones de una playlist en el reproductor :FACU
- IA: Crear un endpoint que me devuelva todas las canciones que escuche: Vicky
- App: En la biblioteca mostrar seccion de canciones escuchadas
- App: Agregar algún tipo de barra de busqueda sobre las canciones de mi historial
- AI: Disponibilizar endpoint para borrar el historial de un usuario: Vicky
- App: Ofrecer la posibilidad de borrar todas las canciones de un usuario
- App: Mostrar desde la biblioteca todas las canciones likeadas
- AI: Disponibilizar endpoint para ver todas las canciones a las que un usuario le dio like: Cami

### Épica: Notificaciones
- Notifis: Crear un nuevo servicio que envie notificaciones (?) 
- Nofits: Disponibilizar un endpoint para enviar notificaciones por topico
- Notifs: Subscribirse a las notificaciones de un artista cuando se hace el following
- Notif: Enviar notificaciones a dispositivos
- Notif: Enviar notificaciones diferidas a dispositivos
- Core: Avisar a Notifs que envie la notificacion cuando se cree un nuevo lanzamiento
- App: Subscribir a las notificaciones de otro usuario
- Core: avisar a notifs cuando un usuario crea una nueva playlist publica
- App: Mostrar una gestion de notificaciones, podes desuscribirse a ciertas notificaciones
- App: Que la aplicación se abra en la pantalla correcta con respecto a las notificaciones
- App que la aplicación le consulte al servicio de notificaciones las notificaciones de un usuario
- Nofis: Endpoint para ver las notificaciones de un usuario
- App: Endpoint para marcar como leida una notificación
- Notifs: Creacion de endpoint para configuraciones


## Estado al finalizar el checkpoint

Se pudo finalizar con las cuestioens que habían quedado pendientes de la entrega anterior con respecto a Reproducción y a Artista, y se pudieron implementar en su totalidad las épicas de Notificaciones y Explorar. Con respecto a la épica de Biblioteca, también se pudo implementar pero no se llegaron a integrar a la rama de main de la aplicación algunas funcionalidades para el día de la entrega. 

## Próximos pasos

- Implementar historias obligatorias faltantes (BackOffice e historias de administración)
- Cubrir la cantidad de puntos necesarios de las historias de usuario opcionales
- Preparar Demo final

