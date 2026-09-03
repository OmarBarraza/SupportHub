# IT Support Platform

## Plataforma de Gestión de Servicios TI y Base de Conocimiento con Asistente de Inteligencia Artificial

---

## Descripción del Proyecto

**IT Support Platform** es una plataforma centralizada para la gestión de servicios de Tecnologías de la Información (TI), diseñada para mejorar la atención, seguimiento y resolución de incidentes y solicitudes de soporte dentro de una organización.

Actualmente, las solicitudes de soporte pueden gestionarse mediante diferentes canales de comunicación, como correo electrónico, mensajería instantánea, llamadas telefónicas y comunicación informal. Esta situación puede provocar información fragmentada, pérdida de conocimiento técnico, duplicación de trabajo y dificultades para dar seguimiento a los incidentes.

La plataforma busca centralizar este proceso mediante un sistema que permita registrar, administrar, consultar y dar seguimiento a las solicitudes de soporte, incorporando además un **asistente de Inteligencia Artificial** capaz de consultar una base de conocimiento técnico autorizada para proporcionar recomendaciones relacionadas con los problemas reportados.

---

# Objetivos

## Objetivo General

Desarrollar una plataforma centralizada de gestión de servicios y conocimiento de TI que permita administrar solicitudes de soporte, centralizar información técnica y proporcionar asistencia mediante Inteligencia Artificial.

## Objetivos Específicos

* Permitir a los empleados registrar solicitudes de soporte.
* Permitir adjuntar evidencia relacionada con los incidentes.
* Proporcionar seguimiento al estado de las solicitudes.
* Permitir al personal de soporte clasificar y priorizar incidentes.
* Asignar solicitudes a miembros del equipo de soporte.
* Registrar las acciones realizadas durante la resolución de incidentes.
* Centralizar documentación y conocimiento técnico.
* Implementar un asistente de Inteligencia Artificial para apoyar la resolución de problemas.
* Investigar y evaluar una arquitectura basada en **Retrieval-Augmented Generation (RAG)**.
* Restringir las recomendaciones de la IA a información proveniente de fuentes autorizadas.
* Mantener supervisión humana en incidentes complejos o críticos.
* Generar métricas relacionadas con la operación del servicio de soporte.
* Evaluar la calidad, utilidad y limitaciones del sistema de Inteligencia Artificial.

---

# Características Principales

### Gestión de usuarios

* Registro y administración de usuarios.
* Autenticación.
* Control de acceso basado en roles.
* Administración de permisos.

### Gestión de tickets

* Creación de solicitudes.
* Clasificación de incidentes.
* Priorización.
* Asignación de responsables.
* Cambio de estados.
* Registro de seguimiento.
* Adjuntar evidencia.
* Resolución y cierre de tickets.

### Base de conocimiento

* Registro de documentación técnica.
* Organización por categorías.
* Consulta de información técnica.
* Control de fuentes autorizadas.
* Administración del conocimiento disponible para la IA.

### Asistente de Inteligencia Artificial

El sistema contará con un asistente de IA orientado a proporcionar apoyo durante la atención de incidentes.

La arquitectura será investigada y evaluada durante el desarrollo del proyecto, considerando alternativas como:

* Retrieval-Augmented Generation (RAG).
* Modelos de lenguaje desplegados localmente.
* APIs externas de modelos de lenguaje.
* Arquitecturas híbridas.
* Recuperación de información desde la base de conocimiento.
* Integración con historial de tickets cuando resulte apropiado.

La IA no tendrá autorización para ejecutar automáticamente acciones administrativas destructivas o críticas.

### Métricas

La plataforma permitirá recopilar información relacionada con:

* Número de solicitudes.
* Solicitudes abiertas y cerradas.
* Tiempo de resolución.
* Prioridades.
* Categorías de incidentes.
* Carga de trabajo.
* Rendimiento del servicio de soporte.

---

# Arquitectura General

El sistema será desarrollado utilizando una arquitectura modular compuesta principalmente por:

```text
                    ┌─────────────────────┐
                    │       Frontend      │
                    │   Web / Interface   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │       Backend       │
                    │       API /         │
                    │    Business Logic   │
                    └──────┬───────┬──────┘
                           │       │
                  ┌────────┘       └────────┐
                  ▼                         ▼
        ┌─────────────────┐       ┌─────────────────┐
        │    Database     │       │   AI / RAG      │
        │                 │       │     System      │
        └─────────────────┘       └────────┬────────┘
                                           │
                                           ▼
                                  ┌─────────────────┐
                                  │ Knowledge Base  │
                                  │ Authorized Docs │
                                  └─────────────────┘
```

---

# Tecnologías

Las tecnologías definitivas podrán modificarse durante la etapa de investigación y diseño.

## Backend

* NestJS
* TypeScript
* Prisma ORM
* REST API

## Frontend

* TypeScript
* [Framework Frontend por definir]
* [Librerías adicionales por definir]

## Base de Datos

* [Base de datos por definir]

## Inteligencia Artificial

* Large Language Model (LLM)
* Retrieval-Augmented Generation (RAG)
* Embeddings
* Vector Database
* Knowledge Base

## Control de Versiones

* Git
* GitHub

## Gestión del Proyecto

* Scrum
* Trello
* Google Drive
* Discord / WhatsApp

## Diseño

* Figma

---

# Estructura del Repositorio

```text
it-support-platform/
│
├── .github/
│   ├── workflows/
│   ├── ISSUE_TEMPLATE/
│   └── pull_request_template.md
│
├── backend/
│   ├── src/
│   ├── prisma/
│   └── test/
│
├── frontend/
│   ├── src/
│   └── public/
│
├── docs/
│   ├── architecture/
│   ├── api/
│   ├── database/
│   ├── ai/
│   └── development/
│
├── tests/
│   ├── integration/
│   ├── e2e/
│   └── ai/
│
├── scripts/
│
├── .gitignore
├── README.md
└── LICENSE
```

---

# Organización del Proyecto

El desarrollo se gestionará utilizando **Scrum** como marco de trabajo.

El equipo trabajará mediante Sprints, utilizando un tablero Kanban en Trello para administrar las actividades.

El flujo general será:

```text
Product Backlog
       │
       ▼
Sprint Planning
       │
       ▼
Sprint Backlog
       │
       ▼
     To Do
       │
       ▼
  In Progress
       │
       ▼
Code Review / Testing
       │
       ▼
      Done
       │
       ▼
Sprint Review
       │
       ▼
Retrospective
```

---

# Equipo

| Integrante               | Rol principal                    |
| ------------------------ | -------------------------------- |
| **Omar Alvarez Barraza** | Team Leader / FullStack Engineer |
| **Oscar Orozco Campos**  | FullStack Engineer / FrontEnd    |
| **Eduardo Contreras**    | FullStack Engineer / UX/UI       |

### Omar Alvarez Barraza

Responsabilidades principales:

* Liderazgo técnico.
* Arquitectura del sistema.
* Desarrollo Backend.
* Desarrollo Frontend.
* Diseño de base de datos.
* Investigación e implementación de IA/RAG.
* Seguridad.
* Integración de componentes.
* Testing.
* Deployment.
* Gestión técnica del proyecto.

### Oscar Orozco Campos

Responsabilidades principales:

* Desarrollo Frontend.
* Arquitectura Frontend.
* Componentes de interfaz.
* Integración con API.
* Dashboard.
* Integración del asistente de IA.
* Pruebas Frontend.

### Eduardo Contreras

Responsabilidades principales:

* UX/UI.
* Investigación de experiencia de usuario.
* User flows.
* Wireframes.
* Prototipos.
* Design System.
* Usabilidad y accesibilidad.
* Diseño de la interfaz del asistente de IA.
* Apoyo al desarrollo Frontend.

---

# Estrategia de Branches

La rama principal será:

```text
main
```

Esta rama contendrá versiones estables del proyecto.

La rama de integración será:

```text
develop
```

Las funcionalidades se desarrollarán mediante ramas independientes:

```text
feature/nombre-funcionalidad
```

Ejemplos:

```text
feature/authentication
feature/ticket-management
feature/knowledge-base
feature/ai-assistant
feature/rag-system
feature/frontend-dashboard
```

Para correcciones:

```text
bugfix/nombre-del-error
```

Para documentación:

```text
docs/nombre-documentacion
```

Para tareas de mantenimiento:

```text
chore/nombre-tarea
```

---

# Flujo de Desarrollo

Cada funcionalidad seguirá aproximadamente este proceso:

```text
Trello Task
     │
     ▼
GitHub Issue
     │
     ▼
Feature Branch
     │
     ▼
Development
     │
     ▼
Testing
     │
     ▼
Pull Request
     │
     ▼
Code Review
     │
     ▼
Approved
     │
     ▼
Merge
     │
     ▼
Develop
```

Las modificaciones importantes no deberán realizarse directamente sobre `main`.

---

# Pull Requests

Cada Pull Request deberá incluir:

* Descripción de los cambios.
* Issue relacionada.
* Funcionalidades implementadas.
* Pruebas realizadas.
* Posibles problemas conocidos.
* Actualización de documentación cuando sea necesaria.

Antes de realizar un merge se deberá comprobar que:

* El código funciona correctamente.
* Las pruebas relevantes fueron ejecutadas.
* No existen credenciales o secretos expuestos.
* La implementación cumple los requisitos.
* La documentación necesaria fue actualizada.

---

# Seguridad

El proyecto deberá considerar la protección de información sensible.

### Nunca subir al repositorio:

```text
.env
.env.local
.env.production
```

ni archivos que contengan:

* Contraseñas.
* API Keys.
* JWT Secrets.
* Credenciales de bases de datos.
* Tokens.
* Access Keys.
* Información personal real.
* Configuraciones sensibles de infraestructura.

En su lugar se utilizará:

```text
.env.example
```

con valores de ejemplo.

Ejemplo:

```env
DATABASE_URL=
JWT_SECRET=
AI_API_KEY=
PORT=3000
```

La Inteligencia Artificial deberá trabajar únicamente con información autorizada y no deberá ejecutar automáticamente acciones administrativas destructivas o críticas.

---

# Documentación

La documentación técnica relacionada con el código se almacenará dentro de:

```text
docs/
```

La documentación académica, evidencias, reuniones, reportes y registros del proyecto se gestionarán mediante Google Drive.

La separación de responsabilidades será:

```text
Trello
└── Qué tenemos que hacer

GitHub
└── Código y control de versiones

Google Drive
└── Documentación y evidencias

Figma
└── Diseño UX/UI

Discord / WhatsApp
└── Comunicación
```

---

# Estado del Proyecto

**Estado actual:** En desarrollo.

Las tecnologías, arquitectura de Inteligencia Artificial, base de datos y componentes específicos podrán evolucionar conforme avance la investigación y desarrollo del proyecto.

---

# Licencia

Este proyecto fue desarrollado con fines académicos.

La licencia definitiva será definida por el equipo conforme a las necesidades del proyecto.
