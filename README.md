# G-COD — Sistema de Gestión de Citas Odontológicas

G-COD es un proyecto de software orientado a la gestión de citas odontológicas y a la organización de los procesos relacionados con la atención de pacientes.

## 📋 Descripción

El proyecto tiene como objetivo desarrollar un sistema que permita gestionar de manera organizada la información y los procesos relacionados con una clínica odontológica.

Actualmente, el repositorio se encuentra en proceso de definición, documentación y organización de los requerimientos funcionales del sistema.

## 🎯 Objetivo

Desarrollar un sistema de gestión de citas odontológicas que facilite la organización de la información y los procesos relacionados con usuarios, pacientes y citas, estableciendo una base para el desarrollo posterior del sistema.

## 📝 Requerimientos funcionales

Los requerimientos funcionales del proyecto se encuentran documentados dentro de la carpeta `Docs/Requisitos/`.

Actualmente se encuentran documentados los siguientes requerimientos:

* **RF1 — Gestión de usuarios y autenticación**
* **RF2 — Gestión de pacientes**
* **RF3 — Gestión de citas**

### RF1 — Gestión de usuarios y autenticación

Documento:

`Docs/Requisitos/RF1-gestion-usuarios.md`

Este requerimiento define la gestión de usuarios y autenticación del sistema.

Incluye aspectos como:

* Registro de usuarios.
* Inicio de sesión.
* Asignación de roles y permisos.
* Autenticación multifactorial.
* Cierre de sesión.
* Activación y desactivación de cuentas.
* Actualización de cuentas.
* Recuperación de contraseña.

Los roles contemplados son:

* Administrador.
* Odontólogo.
* Auxiliar/recepcionista.
* Paciente.

### RF2 — Gestión de pacientes

Documento:

`Docs/Requisitos/RF2-gestion-pacientes.md`

Este requerimiento contiene la documentación correspondiente a la gestión de pacientes del sistema.

### RF3 — Gestión de citas

Documento:

`Docs/Requisitos/RF3-gestion-citas.md`

Este requerimiento contiene la documentación correspondiente a la gestión de citas del sistema.

## 📁 Estructura actual del repositorio

```text
G-COD/
│
├── .github/
│   └── workflows/
│       └── ci.yml
│
├── Docs/
│   └── Requisitos/
│       ├── RF1-gestion-usuarios.md
│       ├── RF2-gestion-pacientes.md
│       └── RF3-gestion-citas.md
│
└── README.md
```

## 🔄 Integración continua

El repositorio cuenta con un flujo básico de Integración Continua mediante **GitHub Actions**.

El archivo de configuración se encuentra en:

```text
.github/workflows/ci.yml
```

El flujo permite realizar validaciones automáticas del repositorio cuando se realizan cambios.

Actualmente, el proceso de integración continua verifica aspectos básicos de la estructura y configuración del repositorio.

## 🌿 Control de versiones

El proyecto utiliza **Git** para el control de versiones y **GitHub** como plataforma para alojar y gestionar el repositorio.

Los cambios realizados en el proyecto se registran mediante commits, permitiendo mantener un historial de las modificaciones.

El trabajo se gestiona mediante ramas y solicitudes de incorporación de cambios (**Pull Requests**) para integrar las modificaciones al repositorio principal.

## 📚 Documentación

La documentación disponible actualmente se encuentra organizada dentro de la carpeta:

```text
Docs/
```

Dentro de ella se encuentra:

```text
Docs/Requisitos/
```

Esta carpeta contiene la documentación correspondiente a los requerimientos funcionales definidos hasta el momento.

A medida que avance el desarrollo del proyecto, se incorporará nueva documentación relacionada con las diferentes etapas del sistema.

## 🚧 Estado del proyecto

**En desarrollo.**

Actualmente, el proyecto se encuentra en la etapa de definición, documentación y organización de sus requerimientos funcionales, junto con la configuración inicial del flujo de integración continua.

---

**G-COD — Sistema de Gestión de Citas Odontológicas**
