---
title: Entrega 4 (Final)
parent: Entregas
nav_order: 4
---

# Entrega 4 — Entrega final

## Objetivos del checkpoint

- Entrega final con foco en calidad y cierre de documentación

## Arquitectura final (snapshot)

- Diagrama final de despliegue y componentes

```mermaid
flowchart TB
  users[Usuarios] --> bff[BFF]
  bff --> auth[Auth]
  bff --> catalogo[Catálogo]
  bff --> playlists[Playlists]
  bff --> streaming[Streaming]
  streaming --> cdn[(CDN)]
  catalogo --> db1[(DB Catálogo)]
  playlists --> db2[(DB Playlists)]
  auth --> db3[(DB Usuarios)]
```

## Decisiones tomadas (resumen)

- Lista de ADRs aceptadas y su impacto

## Estado final y errores conocidos

- Ver sección "Estado, funcionalidades y errores"

## Lecciones aprendidas (cierre)

- Principales aprendizajes y recomendaciones

## Demos finales

- Video de walkthrough end-to-end

## Anexos

- Referencias, links a PRs, issues clave
