# Prueba Técnica – Fullstack

### Contexto

Se requiere extender y completar el servicio de usuarios sobre un proyecto real existente, utilizando Node.js, Express y TypeScript, bajo el enfoque de Arquitectura Hexagonal (Ports & Adapters).

🔗 Repositorio base: **https://github.com/CymetriaGroup/test-back**

El repositorio ya contiene una implementación parcial del servicio de usuarios y define convenciones arquitectónicas que deben respetarse.

### Objetivo de la prueba 

- Comprender y extender un código existente se aceptan mejoras.

- Aplicar arquitectura hexagonal de forma correcta y pragmática.

- Tomar decisiones técnicas fundamentadas, especialmente en escenarios de       escalabilidad.

Escribir código limpio, mantenible y testeable.

Integrar un frontend moderno de forma eficiente.

Comunicar decisiones técnicas de manera clara.

## ⛔ Uso de Inteligencia Artificial (Prohibido)

Queda estrictamente prohibido el uso de cualquier herramienta de Inteligencia Artificial durante el desarrollo de esta prueba técnica.

**Esto incluye (sin excepción):**

- ChatGPT, Claude, Gemini o similares.

- GitHub Copilot u otros asistentes de código.

- Herramientas de autocompletado basadas en IA.

- Generadores automáticos de documentación o tests.

La detección de código generado o asistido por IA será considerada motivo de descalificación inmediata, independientemente de la calidad del resultado.

Esta prueba busca evaluar criterio técnico, experiencia real y capacidad de razonamiento, no la habilidad para formular prompts.

### Alcance y Requerimientos
#### 1. Backend – CRUD de Usuarios:

- Completar el CRUD completo del servicio de usuarios:

- Crear usuario

- Obtener usuario por ID

- Actualizar usuario

- Eliminar usuario

- Listar usuarios con paginación obligatoria

 **Requisitos técnicos**

    Endpoint: GET /api/v1/users

   Debe soportar paginación (page, pageSize o equivalente).

   **La respuesta debe incluir información estructural:**

    data

    page

    pageSize

    total

    totalPages

- El orden de resultados debe ser determinístico.
- Dominio completamente aislado de frameworks (Express, ORM, DB).
- Uso correcto de puertos (interfaces) y adaptadores.
- Evitar lógica de negocio en controladores.
- Manejo explícito de errores de dominio y de infraestructura.

#### 2. Backend – Exportación de Usuarios (Escalabilidad)

Implementar un servicio que permita descargar usuarios en formato Excel.

Escenario crítico

En un escenario con más de **5.000 usuarios**, la generación del archivo no debe bloquear la aplicación ni degradar la experiencia del usuario.

**Se espera que el candidato:**

- Diseñe una estrategia escalable.

- Implemente la solución.

- Documente brevemente el razonamiento técnico.

**Ejemplos válidos de soluciones (no excluyentes):**

- Generación del archivo mediante streaming.

- Uso de CSV compatible con Excel como solución de alto rendimiento.

- Exportación asíncrona (background job) con entrega inmediata si el archivo ya existe.

- Cacheo de exportaciones recientes.

**⚠️ No se espera una solución “perfecta”, sino una solución bien razonada y alineada a un contexto real.**

#### 3. Pruebas Unitarias

- Agregar al menos 2 pruebas unitarias, con enfoque en calidad:

- Prueba de un caso de uso / servicio de aplicación.

- Prueba de un adaptador (controlador o repositorio), usando mocks.

**Se evaluará:**

- Aislamiento correcto del dominio.

- Uso adecuado de mocks/stubs.

- Tests que validen comportamiento, no solo implementación.

#### 4. Frontend – Interfaz de Usuarios

Desarrollar una interfaz web para consumir los servicios implementados.

**Stack recomendado**

- React con Next.js

- React Query

- Zustand para estado global (cuando sea pertinente)

- Tailwind CSS

- UI library opcional: DaisyUI, shadcn/ui u otra equivalente

**Funcionalidades mínimas**

- Listado paginado de usuarios.

- Crear, editar y eliminar usuarios.

- Descarga de usuarios (export).

- Manejo correcto de estados: loading, error, empty.

- UX clara y profesional.

### 5. Entregables

Código entregado mediante el subir un repositorio a github (Puede subir ambos proyectos en el mismo repositorio).

**Instrucciones claras para:**

- Levantar backend.

- Levantar frontend.

- Ejecutar tests.

- Breve documentación (README o documento):

- Decisiones técnicas relevantes.

- Justificación de la estrategia de exportación.

- Consideraciones de escalabilidad.

## Criterios de Evaluación

**A. Arquitectura y diseño (30 pts)**

- Correcta aplicación de arquitectura hexagonal.

- Buen diseño de puertos y adaptadores.

- Código desacoplado, coherente y extensible.

** B. Calidad del CRUD y paginación (20 pts) **

- CRUD completo y consistente.

- Paginación correcta y robusta.

- Manejo de errores y edge cases.

**C. Escalabilidad y exportación (20 pts)**

- Estrategia adecuada para grandes volúmenes de datos.

- Uso eficiente de recursos.

- Buen criterio técnico en la solución propuesta.

**D. Pruebas unitarias (15 pts)**

- Tests bien pensados y útiles.

- Correcto aislamiento de dependencias.


**E. Frontend (15 pts)**

- Integración limpia con el backend.

- Buen uso de React Query y estado.

- Código organizado y mantenible.

### Bonus (hasta +10 pts)

- Documentación clara y concisa.

- Excelente comunicación técnica.

- Buenas prácticas adicionales (linting, estructura, commits claros).

- Propuestas de mejora al proyecto base.

- Funcionalidades adicionales a las mencionadas en el reto.




# 🧠 Si estás leyendo esto… tenemos noticias

Si llegaste hasta aquí, hay dos posibilidades:

- Leíste todo con atención (bien).

- Scrolleaste hasta el final buscando esto (también bien).

**Ahora sí, la verdad:**

👉 Sí, puedes usar IA. Obvio. Solo queríamos asustarte un poco.

**Puedes usar:**

- ChatGPT, Claude Code, Gemini, Codex, etc.

- Github Copilot, Cursor, Antigravity, etc. 

La IA que usas todos los días para trabajar

Incluso Google con respuestas sospechosamente buenas

**📌 PERO:**

No hay peros, por que esta prueba se realizo parcialmente con IA también 😁.

**Y ahora el bonus:**

🎁 Si te asustaste al inicio y aun así leíste todo el documento, te regalamos estas frases:

    Leer hasta el final también es una habilidad técnica.

    El código se copia. El criterio no.

    Ser senior no es escribir más código, es saber cuándo no escribirlo.
 
### Te deseamos mucha suerte 😎