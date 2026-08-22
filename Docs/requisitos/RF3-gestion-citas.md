# RF3 — Gestión de citas

## 1. Descripción general del módulo

El módulo de Gestión de citas se encarga de administrar la programación, modificación, cancelación y visualización de las citas odontológicas. También permite el envío de recordatorios a los pacientes y organiza la agenda de los odontólogos, contribuyendo a evitar cruces de horario y mantener informados a los pacientes.

## 2. Requerimientos funcionales

### RF3.1 — Programar cita

Permite programar una cita odontológica para un paciente previamente registrado y activo.

### RF3.2 — Modificar cita

Permite modificar una cita previamente registrada que se encuentre en estado «Programada».

### RF3.3 — Cancelar cita

Permite cancelar una cita previamente registrada que se encuentre en estado «Programada».

### RF3.4 — Visualizar agenda

Permite visualizar la agenda de citas de los odontólogos.

### RF3.5 — Enviar recordatorios

Permite enviar recordatorios correspondientes a las citas programadas próximas.

## 3. Dependencias

El módulo de Gestión de citas presenta las siguientes dependencias:

- **RF2.1 → RF3.1:** el paciente debe estar previamente registrado y activo para poder programarle una cita.
- **RF3.1 → RF3.2:** la cita debe existir y encontrarse en estado «Programada» para poder modificarla.
- **RF3.1 → RF3.3:** solo pueden cancelarse citas previamente registradas y en estado «Programada».
- **RF3.1 → RF3.5:** debe existir una cita programada próxima dentro del rango configurado para enviar el recordatorio.

## 4. Resumen

El módulo de Gestión de citas administra el ciclo de las citas odontológicas, desde su programación hasta su modificación, cancelación, visualización y recordatorio. Su funcionamiento depende principalmente de que el paciente haya sido previamente registrado y de que la cita exista para realizar las operaciones posteriores.