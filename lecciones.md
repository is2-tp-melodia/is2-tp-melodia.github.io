---
title: Problemas y lecciones aprendidas
nav_order: 4
---
# Problemas encontrados y lecciones aprendidas

A lo largo del desarrollo de Melodia atravesamos múltiples desafíos técnicos, organizativos y de integración entre equipos. Esta sección resume los principales obstáculos, el análisis de sus causas y las mejoras que incorporamos en nuestro proceso de trabajo.

## Problemas destacados

### 1. Curva de aprendizaje y selección de herramientas
Uno de los primeros desafíos fue elegir el stack tecnológico adecuado para cada servicio del ecosistema (Core, Auth, AI, Gateway y BackOffice). La variedad de opciones disponibles —frameworks web, proveedores cloud, bases de datos, librerías de autenticación, herramientas de monitoreo, etc.— implicó un proceso de evaluación más largo de lo esperado.  

A esto se sumó la dificultad de aprender simultáneamente tecnologías nuevas (FastAPI, TypeORM, Firebase, MongoDB, Dokploy, entre otras) mientras avanzábamos con los desarrollos comprometidos por checkpoint.

### 2. Infraestructura y despliegue en la nube
Configurar la infraestructura también representó un desafío significativo:  
- decidir dónde hostear cada servicio,  
- cómo desplegar de forma consistente,  
- cómo monitorear el uso de CPU/memoria,  
- cómo manejar backups y migraciones de bases de datos,  
- y cómo exponer servicios externos de forma segura.  

Si bien finalmente adoptamos Vultr + Dokploy y Supabase/MongoDB Atlas, el análisis inicial y las sucesivas iteraciones consumieron tiempo del equipo y generaron ajustes constantes.

### 3. Falta de planificación inicial y coordinación entre equipos
Durante los primeros checkpoints hubo dificultades para organizar responsabilidades, definir prioridades y sincronizar avances entre App, Core, Auth, AI y BackOffice.  

Esto llevó a:
- esfuerzos duplicados,  
- decisiones tomadas de forma aislada entre equipos,  
- funcionalidades que avanzaban sin un consenso común,  
- y cambios tardíos en APIs ya integradas.

### 4. Ausencia de un codebase y patrones de diseño unificados
Cada repositorio evolucionó a distinto ritmo y con estilos diferentes. En consecuencia, aparecieron **múltiples patrones, convenciones y estructuras de carpetas incompatibles entre sí**, especialmente en Core y Auth.  

Esto hizo más difícil mantener coherencia, reutilizar código, o incorporar nuevas personas en una parte del proyecto sin antes “traducir” el estilo de ese servicio.

### 5. Problemas de modelado y relaciones circulares
El diseño de las bases de datos —en Core— presentó varios casos de relaciones circulares o dependencias difíciles de modelar. Resolverlas requirió iteraciones sucesivas, reescritura de entidades y rediseño del acceso a datos para evitar efectos colaterales.

### 6. Evolución constante del producto y cambios sobre código ya existente
Melodia fue un proyecto cuyo alcance creció progresivamente. Muchos endpoints, entidades y flujos debieron extenderse para soportar:
- el BackOffice,  
- nuevas funcionalidades de Artista y Biblioteca,  
- métricas centralizadas,  
- módulo de notificaciones.

Esto implicó modificar código que ya estaba integrado en la app, generando deuda técnica y situaciones donde agregar una funcionalidad requería actualizar varias capas (Auth, Core, AI, App, BackOffice).

### 7. Campos faltantes y ajustes estructurales tardíos
A medida que avanzábamos, descubrimos que ciertas tablas o modelos no incluían información necesaria para nuevas funcionalidades. Esto derivó en:
- migraciones adicionales,  
- cambios en APIs ya consumidas,  
- y necesidad de sincronizar nuevamente entre equipos para evitar inconsistencias.

### 8. Organización personal y carga académica externa
Finalmente, la coordinación interna del equipo también se vio afectada por la carga de otras materias y trabajos. Mantener una planificación efectiva por checkpoint fue uno de los aspectos más desafiantes del proyecto.

---

## Lecciones aprendidas

### 1. Mantener una comunicación fluida y transversal entre los equipos
El proyecto nos mostró que la comunicación temprana es clave para evitar implementaciones incompatibles, duplicación de esfuerzos y decisiones tomadas en forma aislada. Acordar flujos, contratos de APIs y responsabilidades antes de comenzar a desarrollar reduce retrabajo y mejora la cohesión del sistema.

### 2. Diseñar APIs y modelos de datos más genéricos y extensibles
Aprendimos la importancia de evitar acoplamientos innecesarios en los modelos, endpoints y servicios. Un diseño más genérico permite incorporar nuevas funcionalidades sin tener que modificar muchas funciones ni romper firmas existentes.

### 3. Elegir tecnologías considerando la curva de aprendizaje del equipo
Si bien se probaron tecnologías modernas e interesantes, en varios momentos la curva de aprendizaje ralentizó el progreso. Es fundamental priorizar stacks en los que el equipo tenga experiencia o donde la documentación y el ecosistema reduzcan la complejidad inicial.

### 4. Establecer un codebase consistente desde el inicio
Definir estándares de código, estructura de carpetas, acuerdos de nomenclatura y patrones de diseño desde el checkpoint 1 hubiera evitado inconsistencias entre microservicios. La homogeneidad facilita el mantenimiento y acelera el onboarding de cualquier integrante.

### 5. Planificación más rigurosa por checkpoint
Una de las lecciones más claras es la necesidad de mejorar cómo organizamos las tareas, el alcance de cada entrega y la asignación de responsables. Dedicar tiempo a la planificación nos hubiese permitido prever dependencias entre equipos, distribuir carga de manera más equilibrada y evitar cambios de último momento.

### 6. Validar modelados y relaciones desde etapas tempranas
Los problemas de relaciones circulares y campos faltantes mostraron la importancia de revisar el modelado con una visión completa del dominio desde el inicio. Esto reduce migraciones, reescritura de entidades y cambios de API a mitad del proyecto.

### 7. Priorizar el diseño modular para soportar cambios futuros
Dado que Melodia evolucionó mucho entre checkpoints, confirmamos que la arquitectura debe poder adaptarse a nuevas épicas sin obligar a reescribir grandes partes del sistema. Un diseño modular y desacoplado simplifica la evolución del producto.

---

