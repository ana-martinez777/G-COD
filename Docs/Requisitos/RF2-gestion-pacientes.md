# RF2 - Gestión de Pacientes

> **Requerimiento Funcional RF2** del Sistema de Gestión de Citas Odontológicas.

## 📌 Descripción

El módulo de **Gestión de Pacientes** permite administrar la información de las personas que utilizan los servicios de la clínica odontológica.

Su propósito es centralizar y mantener actualizados los datos de los pacientes, facilitando su registro, consulta y actualización. La información registrada podrá ser utilizada posteriormente en procesos como la programación de citas, consulta de la historia clínica y seguimiento de la atención odontológica.

El módulo busca reducir el uso de registros manuales y evitar la duplicidad o pérdida de información de los pacientes.

---

## 🎯 Objetivo

Garantizar que la información de los pacientes sea:

- Correcta.
- Completa.
- Actualizada.
- Disponible para los usuarios autorizados.
- Organizada para facilitar su consulta.
- Protegida mediante los mecanismos de seguridad del sistema.

---

## ✅ Funcionalidades

| ID | Funcionalidad | Descripción | Prioridad |
|---|---|---|---|
| RF2.1 | Registrar pacientes | Permite registrar un nuevo paciente con sus datos personales y de contacto. | Alta |
| RF2.2 | Consultar pacientes | Permite buscar y visualizar la información registrada de un paciente. | Alta |
| RF2.3 | Actualizar datos | Permite modificar la información personal o de contacto de un paciente. | Alta |
| RF2.4 | Gestionar estado | Permite cambiar el estado de un paciente según las condiciones definidas por el sistema. | Media |
| RF2.5 | Consultar información relacionada | Permite acceder a información relacionada con las citas e historia clínica del paciente. | Media |

---

## 📝 RF2.1 - Registrar pacientes

El sistema debe permitir al usuario autorizado registrar nuevos pacientes.

### Datos principales

- Tipo de documento.
- Número de documento.
- Nombres.
- Apellidos.
- Fecha de nacimiento.
- Género.
- Teléfono.
- Correo electrónico.
- Dirección.
- Información de contacto de emergencia.
- Estado del paciente.

### Validaciones

- Los campos obligatorios deben estar completos.
- El número de documento no debe estar registrado previamente.
- El correo electrónico debe tener un formato válido cuando sea requerido.
- El teléfono debe contener únicamente caracteres permitidos.
- El sistema debe informar al usuario cuando exista información inválida.

---

## 🔎 RF2.2 - Consultar pacientes

El sistema debe permitir buscar pacientes registrados.

La búsqueda podrá realizarse utilizando información como:

- Número de documento.
- Nombre.
- Apellido.
- Teléfono.
- Estado del paciente.

Al seleccionar un paciente, el sistema debe mostrar la información registrada y disponible para el usuario según sus permisos.

---

## ✏️ RF2.3 - Actualizar datos de pacientes

El sistema debe permitir modificar los datos de un paciente cuando sea necesario.

Los usuarios autorizados podrán actualizar información como:

- Teléfono.
- Correo electrónico.
- Dirección.
- Datos de contacto.
- Información personal permitida.

Antes de guardar los cambios, el sistema deberá validar la información ingresada.

Los cambios realizados deben quedar almacenados correctamente en el sistema.

---

## 🔄 RF2.4 - Gestionar estado del paciente

El sistema debe permitir administrar el estado de los pacientes.

Los estados pueden utilizarse para identificar si un paciente se encuentra:

- **Activo:** puede utilizar normalmente los servicios del sistema.
- **Inactivo:** no se encuentra activo para nuevos procesos.
- **Restringido:** presenta alguna condición que requiere validación antes de realizar determinadas acciones.

El cambio de estado debe ser realizado únicamente por usuarios que tengan los permisos correspondientes.

---

## 📋 RF2.5 - Información relacionada

La información del paciente podrá relacionarse con otros módulos del Sistema de Gestión de Citas Odontológicas.

Entre la información relacionada se encuentra:

- Citas odontológicas.
- Historia clínica.
- Procedimientos realizados.
- Estado de las citas.
- Información necesaria para la atención del paciente.

Estas relaciones permitirán consultar la información necesaria sin tener que registrar nuevamente los datos del paciente.

---

## 🏢 Reglas de negocio

1. Cada paciente debe tener un documento de identificación único.
2. No se debe permitir registrar dos pacientes con el mismo número de documento.
3. Los campos obligatorios deben ser validados antes de guardar la información.
4. La información del paciente debe mantenerse actualizada.
5. Los datos personales deben manejarse de forma confidencial.
6. Solo los usuarios autorizados podrán modificar determinada información.
7. Un paciente que tenga información relacionada con citas o historia clínica no debe eliminarse directamente de la base de datos.
8. Cuando sea necesario retirar un paciente del funcionamiento normal del sistema, se debe utilizar el cambio de estado.
9. La información registrada debe conservar la integridad de los datos.
10. Las operaciones realizadas deben respetar los permisos definidos para cada usuario.

---

## 👥 Roles involucrados

### Administrador

Puede:

- Registrar pacientes.
- Consultar pacientes.
- Actualizar información.
- Gestionar el estado de los pacientes.
- Administrar los permisos correspondientes.

### Recepcionista

Puede:

- Registrar pacientes.
- Consultar información.
- Actualizar datos permitidos.
- Gestionar información relacionada con las citas.

### Odontólogo

Puede:

- Consultar información de los pacientes.
- Consultar la información necesaria para la atención odontológica.
- Consultar la historia clínica asociada al paciente.

---

## 🗃️ Entidades relacionadas

El módulo de Gestión de Pacientes se relaciona principalmente con:

- **Paciente:** almacena la información principal de la persona.
- **Cita:** permite relacionar al paciente con sus citas odontológicas.
- **Historia Clínica:** almacena información relacionada con la atención odontológica.
- **Procedimiento:** permite relacionar los procedimientos realizados al paciente.
- **Usuario:** determina qué usuarios pueden acceder o modificar información.

---

## 🔐 Seguridad y privacidad

La información almacenada en el módulo debe ser manejada de manera segura.

Se deben considerar los siguientes aspectos:

- Control de acceso según el rol del usuario.
- Protección de los datos personales.
- Validación de la información ingresada.
- Evitar accesos no autorizados.
- No exponer información sensible innecesariamente.
- Mantener la integridad de los registros.

---

## ⚙️ Consideraciones técnicas

- La información de los pacientes será almacenada en la base de datos del sistema.
- El backend será responsable de validar y procesar las solicitudes.
- El frontend permitirá al usuario interactuar con los formularios y consultas.
- Las validaciones deben realizarse tanto en la interfaz como en el backend.
- Las consultas deben estar optimizadas para facilitar la búsqueda de pacientes.
- La información debe mantenerse consistente entre los diferentes módulos del sistema.
- El módulo debe poder integrarse con el sistema de gestión de citas y la historia clínica.

---

## 🔗 Relación con otros requerimientos

El RF2 tiene relación con otros procesos del Sistema de Gestión de Citas Odontológicas, especialmente:

- **Gestión de citas:** cada cita debe estar asociada a un paciente registrado.
- **Historia clínica:** la información clínica debe relacionarse con el paciente correspondiente.
- **Gestión de usuarios:** los permisos determinan qué operaciones puede realizar cada usuario.
- **Reportes:** la información de pacientes puede ser utilizada para generar reportes del sistema.

---

## 📌 Flujo general

1. El usuario autorizado ingresa al módulo de Gestión de Pacientes.
2. El sistema muestra las opciones disponibles según su rol.
3. El usuario selecciona registrar, consultar o actualizar un paciente.
4. El sistema solicita o muestra la información correspondiente.
5. Se realizan las validaciones necesarias.
6. Si la información es válida, el sistema guarda o actualiza los datos.
7. El sistema muestra una confirmación de la operación.
8. La información queda disponible para los procesos relacionados.

---

## ⚠️ Manejo de errores

El sistema debe informar claramente al usuario cuando ocurra alguna situación como:

- El paciente ya se encuentra registrado.
- El número de documento ya existe.
- Faltan campos obligatorios.
- Los datos ingresados no tienen un formato válido.
- No se encuentra el paciente solicitado.
- El usuario no tiene permisos para realizar la operación.
- Se presenta un error durante el almacenamiento de la información.

Los mensajes deben ser claros y permitir que el usuario identifique cómo corregir el problema cuando sea posible.

---

## 📊 Criterios de aceptación

El requerimiento se considera cumplido cuando:

- [ ] Es posible registrar un nuevo paciente.
- [ ] El sistema valida los campos obligatorios.
- [ ] El sistema evita duplicar pacientes por número de documento.
- [ ] Es posible consultar pacientes registrados.
- [ ] Es posible buscar pacientes mediante diferentes datos.
- [ ] Es posible actualizar información autorizada.
- [ ] Es posible gestionar el estado del paciente.
- [ ] La información queda almacenada correctamente.
- [ ] Los permisos de acceso se respetan.
- [ ] La información puede relacionarse con citas e historia clínica.
- [ ] Los errores son informados correctamente al usuario.

---

## 📦 Resultado esperado

El módulo de Gestión de Pacientes debe proporcionar una forma organizada y segura de administrar la información de los pacientes de la clínica odontológica.

Con este módulo se busca mejorar la disponibilidad de la información, reducir errores de registro, evitar duplicidad de datos y facilitar la integración con los demás procesos del sistema.

---

## 👤 Responsable

**Laura Daniela Avilés**

## 📅 Fecha

**14/08/2026**

## 📁 Módulo

**RF2 - Gestión de Pacientes**
## Verificación del pipeline

Prueba de ejecución del pipeline mediante push en la rama RF2.
