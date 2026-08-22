# G-COD

Sistema de Gestión de Citas Odontológicas

## Flujo de trabajo con Git

El proyecto utiliza un flujo de trabajo basado en ramas para organizar el desarrollo y facilitar la integración de los cambios.

### Rama principal

- `main`: rama principal del proyecto. Contiene los cambios integrados y revisados.

### Ramas de funcionalidades

Cada integrante trabaja en una rama independiente según la funcionalidad asignada:

- `feature/RF1-gestion-usuarios` — Gestión de usuarios.
- `feature/RF2-gestion-pacientes` — Gestión de pacientes.
- `feature/RF3-gestion-citas` — Gestión de citas.

### Flujo de trabajo

1. Cada integrante desarrolla su funcionalidad en su rama `feature/*`.
2. Los cambios se registran mediante commits.
3. La rama se sube al repositorio remoto mediante `push`.
4. Se crea un Pull Request desde la rama de funcionalidad hacia `main`.
5. Otro integrante revisa los cambios antes de integrarlos.
6. Una vez aprobados los cambios y superadas las comprobaciones del pipeline CI, se realiza el merge hacia `main`.
7. GitHub conserva el historial de commits, Pull Requests, revisiones y merges.

### Integración continua

El proyecto utiliza GitHub Actions para ejecutar automáticamente un pipeline de integración continua.

El workflow se encuentra en:

`.github/workflows/ci.yml`

El pipeline se ejecuta ante cambios en las ramas configuradas y verifica la estructura básica del proyecto.

### Historial y trazabilidad

El historial del proyecto se mantiene visible en GitHub mediante los commits, ramas, Pull Requests, revisiones y merges realizados por los integrantes del equipo.

El flujo utilizado es:

`feature/*` → Pull Request → Revisión de pares → Merge → `main`
