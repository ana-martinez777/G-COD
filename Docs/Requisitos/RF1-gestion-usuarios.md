# RF1 – Gestión de usuarios y autenticación

## 1. Descripción

El módulo de Gestión de usuarios y autenticación administra el registro, la autenticación, la asignación de roles y permisos y el ciclo de vida de las cuentas de los usuarios del sistema.

Los usuarios contemplados en el sistema son:

- Administrador.
- Odontólogo.
- Auxiliar/recepcionista.
- Paciente.

## 2. Objetivo

Garantizar que los usuarios puedan acceder al sistema de manera segura y que cada uno tenga los permisos correspondientes según su rol, permitiendo además administrar el estado y la información de sus cuentas.

## 3. Requerimientos funcionales

### RF1.1 – Registro de usuario

Permite registrar nuevos usuarios en el sistema.

### RF1.2 – Inicio de sesión

Permite que los usuarios registrados y con una cuenta activa puedan ingresar al sistema mediante sus credenciales.

### RF1.3 – Asignar roles y permisos

Permite asignar roles y permisos a los usuarios según las funciones que desempeñan dentro del sistema.

### RF1.3.1 – Autenticación multifactorial

Extiende el proceso de inicio de sesión mediante un segundo factor de autenticación después de validar las credenciales principales.

### RF1.4 – Cerrar sesión

Permite al usuario finalizar de manera segura su sesión activa en el sistema.

### RF1.5 – Desactivación de cuenta

Permite desactivar una cuenta de usuario cuando sea necesario.

### RF1.6 – Activación de cuenta

Permite activar nuevamente una cuenta de usuario que se encuentre desactivada.

### RF1.7 – Actualización de cuenta

Permite actualizar la información asociada a la cuenta del usuario.

### RF1.8 – Recuperar contraseña

Permite al usuario recuperar el acceso a su cuenta cuando no recuerde su contraseña.

## 4. Responsabilidad del módulo

Este módulo es responsable de validar la identidad de los usuarios, controlar el acceso al sistema y definir las acciones permitidas según el rol asignado.

También administra el ciclo de vida de las cuentas y proporciona mecanismos de seguridad como la autenticación, el bloqueo por intentos fallidos y la recuperación de contraseña.

## 5. Dependencias principales

### RF1.1 → RF1.2

El usuario debe estar previamente registrado y tener su cuenta activa para poder iniciar sesión en el sistema.

### RF1.1 → RF1.3

El usuario debe existir previamente en el sistema para poder asignarle un rol y sus respectivos permisos.

### RF1.2 → ERF1.3.1

La autenticación multifactorial extiende el proceso de inicio de sesión y solicita un segundo factor después de validar las credenciales principales.

## 6. Flujo general del módulo

El funcionamiento general del módulo puede representarse de la siguiente manera:

**Registro de usuario → Inicio de sesión → Validación de identidad → Aplicación de roles y permisos → Acceso al sistema**

El módulo permite administrar posteriormente el estado y la información de las cuentas mediante las funciones de activación, desactivación, actualización y recuperación de contraseña.