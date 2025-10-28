---
title: Decisiones de arquitectura
nav_order: 3
---

# Decisiones de arquitectura (ADRs)

Registra decisiones relevantes con su contexto, alternativas y consecuencias. Mantenerlas cortas y accionables.

## Índice de ADRs

- ADR-001: Arquitectura por microservicios vs monolito — Estado: Propuesto/Aceptado
- ADR-002: Tecnología mobile (Flutter/React Native) — Estado: Propuesto/Aceptado
- ADR-003: CDN para contenidos de audio — Estado: Propuesto/Aceptado
- ADR-004: BBDD por servicio — Estado: Propuesto/Aceptado

Sugerencia: cada ADR puede vincular a una ancla en esta misma página o a un documento aparte. Para mantener simple el repositorio, usamos anclas aquí mismo.

---

## ADR-001 — Arquitectura por microservicios vs monolito

- Estado: Propuesto
- Fecha: AAAA-MM-DD

Contexto:
- Requisitos de escalabilidad y equipos trabajando en paralelo.

Decisión:
- Separar en servicios: Auth, Usuarios, Catálogo, Playlists, Streaming, Analytics, con un BFF/API Gateway.

Alternativas consideradas:
- Monolito modular: +simple al comienzo, -escalabilidad, -desacople de despliegue.
- Microservicios con eventos: +escalable, +aislamiento, +autonomía equipos; +complejidad operativa.

Consecuencias:
- DevOps más exigente (observabilidad, CI/CD, versionado de contratos).
- Posibles latencias inter-servicios; mitigación con BFF y caché.

Métricas de éxito:
- Tiempos de ciclo por equipo, MTTR, escalabilidad por servicio.

---

## ADR-002 — Tecnología mobile (Flutter/React Native)

- Estado: Propuesto
- Fecha: AAAA-MM-DD

Contexto:
- Necesidad de cross-platform iOS/Android con equipo acotado.

Decisión:
- Elegir <Flutter/React Native> por <razones>.

Alternativas consideradas:
- Nativo (Kotlin/Swift), Kotlin Multiplatform.

Consecuencias:
- Performance y ecosistema de librerías: verificaciones necesarias para audio/DRM.

---

## ADR-003 — CDN para contenidos de audio

- Estado: Propuesto
- Fecha: AAAA-MM-DD

Contexto:
- Latencia/throughput para streaming.

Decisión:
- Utilizar CDN + almacenamiento de objetos para medios.

Consecuencias:
- Costos variables; estrategia de caching y políticas de invalidez.

---

## ADR-004 — BBDD por servicio

- Estado: Propuesto
- Fecha: AAAA-MM-DD

Contexto:
- Independencia de despliegue y escalado.

Decisión:
- Cada microservicio mantiene su propia base de datos.

Consecuencias:
- Complejidad de reportes multi-servicio; mitigación con capa de analytics y/o eventos.
