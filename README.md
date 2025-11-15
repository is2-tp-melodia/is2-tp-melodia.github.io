# Melodia — Bitácora de Proyecto (IS2 - FIUBA)

Este repositorio publica la documentación del TP "Melodia" como sitio de GitHub Pages. La bitácora se mantiene de forma incremental a través de las 4 entregas.

## Estructura

- `index.md`: portada del sitio y guía de navegación
- `arquitectura.md`: diagramas y decisiones tomadas
- `estado-errores.md`: funcionalidades completas/incompletas y errores conocidos
- `lecciones.md`: problemas encontrados y lecciones aprendidas
- `demos.md`: demos y showcases (opcional)
- `entregas/`: páginas por checkpoint (cp1..cp4)
- `_includes/head_custom.html`: activa Mermaid.js para diagramas
- `assets/img/`: imágenes y diagramas importados
- `_config.yml`: configuración del tema (Just the Docs)

## Publicación en GitHub Pages

Este repositorio está listo para GitHub Pages usando el tema "just-the-docs" (remote theme). Al hacer push en `main`, GitHub genera y publica el sitio automáticamente.

URL de la página: https://is2-tp-melodia.github.io


## Cómo editar contenido

1. Editá los archivos `.md` para actualizar contenido.
2. Para diagramas, usá bloques Mermaid:

	 ```
	 ```mermaid
	 flowchart LR
		 A --> B
	 ```
	 ```

	 Mermaid se incluye automáticamente desde `_includes/head_custom.html`.
3. Subí imágenes a `assets/img/` y referencialas con rutas relativas (ej.: `![alt](assets/img/diagrama.png)`).

## Previsualización local (opcional)

No es necesario para contribuir, pero si querés correrlo localmente:

- Requiere Ruby + Bundler para Jekyll. Alternativamente, podés abrir los `.md` en GitHub y usar la vista publicada.

## Convenciones

- Mantener ADRs cortos y con estado (Propuesto/Aceptado/Desestimado)
- Actualizar la sección "Entregas" en cada checkpoint (snapshot de arquitectura, decisiones, estado, métricas y lecciones)
- Mantener enlaces a PRs/issues cuando corresponda

## Créditos

Ingeniería de Software 2 — FIUBA.
