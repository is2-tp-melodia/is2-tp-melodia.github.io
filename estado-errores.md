---
title: Estado, funcionalidades y errores
nav_order: 3
---

# Estado del proyecto: funcionalidades y errores

---

## 📊 Resumen del estado actual

**Última actualización:** `08/12/2025`
**Estado general:** `🟢 Estable`

| Métrica | Estado |
|---------|--------|
| Funcionalidades de Usuarios  | `🟢 Completadas` |
| Funcionalidades de Perfil  | `🟢 Completadas` |
| Funcionalidades de Artistas | `🟢 Completadas` |
| Funcionalidades de Administración de Contenido | `🟡 Completadas las obligatorias` |
| Funcionalidades de Administración de Usuarios | `🟢 Completadas` |
| Funcionalidades de Explorar  | `🟡 Completadas excepto Made for you` |
| Funcionalidades de Reproducción   | `🟡 Completadas excepto On Demand` |
| Funcionalidades de Métricas | `🟢 Completadas` |
| Funcionalidades de Biblioteca | `🟢 Completadas` |
| Funcionalidades de Notificaciones | `🟢 Completadas` |
| Funcionalidades de Social | `🟢 Completadas` |
| Funcionalidades de Vibras | `🔴 No Completadas` |
| Funcionalidades de Onboarding Usuario | `🟢 Completadas` |

---

## ✅ Funcionalidades completas

- [x] Registro de usuarios
- [x] Login con email y contraseña
- [x] Login con proveedor federado
- [x] Recuperación de contraseña
- [x] Edición de perfil
- [x] Visualización de perfil propio
- [x] Visualización de perfil de otros usuarios
- [x] Perfil del artista
- [x] Discografía
- [x] Colaboraciones (Aparece en)
- [x] Popular (Top del artista)
- [x] Artistas relacionados (Similares a)
- [x] Gestión de perfil del artista
- [x] Publicación de lanzamientos
- [x] Disponibilidad por ventana
- [x] Listar usuarios del sistema
- [x] Visualizar perfil de usuario
- [x] Bloquear usuario
- [x] Catálogo — Explorar y buscar contenido
- [x] Catálogo — Detalle y trazabilidad
- [x] Bloqueo y desbloqueo con alcance
- [x] Transiciones y estado efectivo del catálogo
- [x] Home
- [x] Búsqueda unificada por tipo de contenido
- [x] Navegación a vistas de detalle
- [x] Reproducción y Controles Básicos
- [x] Controles avanzados del Player
- [x] Gestión de cola
- [x] Marcado de Liked Songs desde el Player
- [x] Videos Musicales Asociados
- [x] Reproducción Continua (autoplay) [IA]
- [x] Creación y Gestión de Playlists
- [x] Reordenamiento de Contenido en Playlists
- [x] Historial de Reproducción
- [x] Liked Songs
- [x] Creación Asistida de ‘Mood Mixes’ (IA)
- [x] Notificación por nuevo contenido y actividad seguida
- [x] Enrutamiento al hacer clic en notificaciones (Deep Link)
- [x] Métricas de canciones y álbumes
- [x] Métricas de usuario
- [x] Seguimiento de Perfiles de Usuario
- [x] Compartir Canciones y Playlists
- [x] Auto Play (nuevo contexto) [IA]
- [x] Captura Inicial de Géneros Favoritos
- [x] Asistente de Artistas Favoritos
- [x] Personalización de Notificaciones Iniciales

---

## 🚧 Funcionalidades no implementadas

- [ ] Autocompletar metadatos (“Fast Complete”) [IA]
- [ ] Disponibilidad por región y ventana
- [ ] Made For You
- [ ] Reproducción On Demand
- [ ] Métricas de artistas
- [ ] Visualización de Actividad de Amigos
- [ ] Playlists temáticas por contexto [IA]
- [ ] Radio por Canción [IA]

---

## 🐛 Errores conocidos

### Críticos
> Ningún error crítico con respecto a la aplicacion 🎉

### Altos

#### Errores ocurrentes al crear el perfil de artista con las imagenes

**Descripción:**
Este error se produce cuando a veces se intenta subir una imagen ya encontrada en el sistema, pero actualmente es manejado con un aviso generico que informa al usuario que no se pudo subir su imagen.

---

#### Bug con la carga de canciones por recomendacion de la IA a la cola del reproductor

**Descripción:**
Se produce debido a la latencia en la respuesta del servidor al momento de agregar canciones a la cola del reproductor. Generando que se pause el flujo de canciones.

---

### Medios

#### El reproductor carga completamente la cancion al llegar a una cancion nueva

**Descripción:**
Cuando se avanza a la siguiente canción en la playlist, el reproductor intenta cargar toda la canción antes de comenzar a reproducirla, lo que genera un retraso notable en la experiencia del usuario. Esto es debido al uso de una librería de terceros con la que no se le implemento la optimización de streaming progresivo.

### Bajos

#### Falta de permisos al obtener las playlists privadas (supervisores) (ARREGLADO)

**Descripción:**
Los usuarios con rol de supervisor no podian acceder a las playlists privadas de otros usuarios, lo que limita su capacidad para gestionar y supervisar el contenido adecuadamente.

#### Backoffice no permitia editar un release ya publicado (ARREGLADO)

**Descripción:**
Los usuarios con rol de supervisor no podian editar los detalles de un release debido a un defecto en la visual por parte del backoffice.


## 📈 Métricas de calidad

### Cobertura de tests por módulo

| Módulo | Unit |
|--------|------|
| Auth | 92% |
| Core | 75% |
| IA | 77% |
| Notifications | 88% |
| Gateway | 78% |
| **Promedio global** | **82%** |


## ⚠️ Riesgos identificados

### Performance

Una cosa que notamos fuertemente fue en la baja de performance en la aplicacion debido a la alta demanda de consultas las cuales realizamos. Creemos fielmente que la arquitectura actual es muy buena y bien desarrollada, pero sin embargo, no es suficiente para la demanda que estamos teniendo para un unico usuario y mucho menos para muchos a la vez.

### Fallos ocurrentes

Si bien no tenemos errores criticos, si hemos notado que hay fallos ocurrentes que se nos han escapado de nuestros casos bases y hay algunos que no hemos podido cubrir. Algunos de ellos los hemos logrado mitigar pero otros sabemos que siguen presentes o que hay algunos que desconocemos y pueden surgir. Nos falto hacer mas pruebas manuales siendo nosotros nuestros propios usuarios pero creemos fielmente que nuestro trabajo sigue fielmente solido.

## 🚀 Próximos pasos
Si bien el proyecto se encuentra finalizado, queriamos dejar un listado de posibles mejoras y continuaciones que podrian ser tomadas en cuenta para el futuro.
- Mejorar la cantidad de consultas realizadas.
- Optimizar la reproduccion de audio.
- Optimizar la reproduccion de video.
- Implementar las funcionalidades faltantes.
- Realizar pruebas de carga y stress para verificar la resistencia de nuestra aplicacion y nuestra base.
- Realizar pruebas de usabilidad siendo nosotros mismos los usuarios para verificar la experiencia de usuario y los problemas potenciales actuales.
- Entre otros.

