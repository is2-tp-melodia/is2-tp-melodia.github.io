---
title: Entrega 2
parent: Entregas
nav_order: 2
---

# Entrega 2 — Alcance y avances

## Tareas comprometidas del checkpoint

Para esta entrega se comenzó a incorporar el servicio de Melodia-AI, se implementó Melodia-Gateway y se avanzó y profundizó con Melodia-Core y con la aplicación. Además, se comenzó a utilizar Datadog como herramienta de monitoreo.

### Épica: Reproducción
**Reproducción y Controles Básicos**
- App: Creación de pantalla de reproductor
- App: Manejo de estado de reproductor: Tomi L
- App: Conexión con backend para conseguir track: Tomi L
- Core: Upload y almacenamiento de canciones, endpoint de creación de canciones
- Core: Distribución de tracks
- Controles avanzados del Player: Tomi L

**Gestión de cola**
- App: Manejo de estados: Tomi L
- App: Pantalla de navegación por canciones + Agregado al estado
- Core: Endpoint para listar canciones

**Marcado de Liked Songs desde el Player**
- App: Integración con backend para registrar interacción: Tomi L
- AI: Endpoint para capturar Liked + Reproducción de canciones: Vicky

**Videos Musicales Asociados → OPCIONAL**
- App: consumir videos además de contenido sonoro

**Reproducción On Demand (multidispositivo) → OPCIONAL**

**Reproducción Continua (autoplay) [IA] → OPCIONAL**
- App: Conectar con Melodia AI para informar canción actual y recibir próximas canciones
- AI: Endpoint para recomendar próximas canciones en base a canción brindada: Cami

### Épica: Observabilidad
- Datadog / Alertas sobre uso / Métricas de uso / Logs 
- Configurar alertas sobre uso y salud

### Épica: Artista

**Perfil del artista**
- App: Mostrar perfil del artista
- Core: Retornar información del artista
- App: Conexión y obtener información del artista desde el backend
- AI: Liked Songs

**Discografía**
- Core: Retornar discografía de un artista: Tomi C
- App: Mostrar discografía del artista en la perfil
- App: Conectar con el backend para conseguir la biografía del artista
- Colaboraciones (Aparece en) →  OPCIONAL
- Core: Retornar colaboraciones de una artista
- App: Mostrar colaboraciones del artista en la perfil

**Popular (Top del artista)**
- Core/AI: Retornar canciones populares del artista
- App: Mostrar populares del artista en la su perfil
- App: Conectar dentro del artista los populares desde la app contra el core: Facu

**Artistas relacionados (Similares a)**
- Core: Retornar artistas relacionados del artista: Vicky
- App: Mostrar artistas relacionados al artista en la su perfil
- App: Pedirle al backend que corresponda los datos: Facu

**Gestión de perfil del artista**
- App: Creación de pantalla para editar perfil de artista
- Core: carrusel de imágenes
- App: Conectar aplicación con backend: Facu

**Publicación de lanzamientos**
- App: pantalla para crear un release de draft: Tomi L
- App: pantalla para subir una canción: Tomi L
- Core: endpoints relacionados a tracks y releases

**Disponibilidad por ventana →  OPCIONAL**

**Autocompletar metadatos (“Fast Complete”) [IA] ) →  OPCIONAL**

### Épica: Explorar

**Home**
- Maqueta: Diseño de pantalla home
- App: Implementación de pantalla home
- AI: Respuesta de información inicial para llenar pantalla de home en la app: Cami
- Core: Endpoint para obtener infomación de canciones
- App: Interactuar con backend para conseguir la información necesaria: Ayuda

## Estado al finalizar el checkpoint

Con respecto a las historias de usuario opcionales, se comenzaron a desarrollar las de Videos Musicales Asociados, de Reproducción Continua y Colaboraciones. No se llegaron a finalizar para priorizar las historias obligatorias pero se planea completarlas para la siguiente entrega. Además. no se llegó a terminar de integrar el home del todo con el backend. 

Las demás funcionalidades se completaron exitosamente, faltando solamente pulir algunos aspectos y mejorar un poco el coverage de código. 


## Próximos pasos

- Terminar de pulir las funcionalidades de esta entrega
- Agregar tests faltantes
- Definir historias comprometidas para E3
