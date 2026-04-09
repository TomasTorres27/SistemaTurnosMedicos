# Introducción

## ¿Qué es la Programación Orientada a Objetos?

El paradigma de programación orientado a objetos (POO) es un enfoque de desarrollo de software basado en la representación de elementos del mundo real mediante “objetos”, los cuales contienen datos (atributos) y comportamientos (métodos). Este paradigma se apoya en conceptos fundamentales como la encapsulación, la herencia, el polimorfismo y la abstracción, que permiten organizar y estructurar el código de manera más clara y eficiente.

La importancia de la programación orientada a objetos radica en que facilita el desarrollo de sistemas complejos, como el sistema de turnos médicos, permitiendo dividir el problema en partes más pequeñas y manejables. Además, mejora la reutilización del código, el mantenimiento del sistema y su escalabilidad, ya que los objetos pueden modificarse o ampliarse sin afectar el funcionamiento general del programa.

En este trabajo, la aplicación de este paradigma permite modelar entidades como pacientes, médicos y turnos de forma lógica y ordenada, reflejando situaciones reales dentro del sistema.

---

## Los cuatro pilares de la POO

### Encapsulamiento
El encapsulamiento consiste en ocultar los datos internos de un objeto y permitir el acceso a ellos solo mediante métodos definidos.

### Abstracción
La abstracción permite representar solo las características esenciales de un objeto, ignorando los detalles innecesarios.

### Herencia
La herencia permite que una clase reutilice atributos y métodos de otra.

### Polimorfismo
El polimorfismo permite que un mismo método se comporte de diferentes maneras según el objeto que lo utilice.

---

## Requisitos iniciales del sistema

### Requisitos funcionales

Requisitos funcionales

Los requisitos funcionales describen qué debe hacer el sistema.

- Registro de pacientes
El sistema debe permitir registrar nuevos pacientes ingresando datos como nombre, DNI y datos de contacto.
- Registro de médicos
El sistema debe permitir cargar médicos con su especialidad, nombre y disponibilidad horaria.
- Asignación de turnos
El sistema debe permitir asignar turnos a los pacientes con un médico disponible en una fecha y hora determinada.
- Cancelación de turnos
El sistema debe permitir cancelar turnos previamente asignados, liberando ese horario.
- Consulta de turnos
El sistema debe permitir visualizar los turnos asignados, ya sea por paciente, médico o fecha.

### Requisitos no funcionales

Los requisitos no funcionales describen cómo debe funcionar el sistema.

- Usabilidad
El sistema debe ser fácil de usar, con una interfaz clara e intuitiva para el usuario.
- Rendimiento
El sistema debe responder rápidamente a las solicitudes, como la asignación o consulta de turnos.
- Seguridad
Los datos de pacientes y médicos deben estar protegidos y no ser accesibles por usuarios no autorizados.
- Disponibilidad
El sistema debe estar disponible en todo momento para permitir la gestión de turnos sin interrupciones.
- Escalabilidad
El sistema debe poder adaptarse al crecimiento, permitiendo agregar más pacientes, médicos y turnos sin afectar su funcionamiento.

---
# Casos de Uso - Sistema de Turnos Médicos

---

## Caso de Uso 1: Registrar paciente

**Actor(es):** Secretaria Valeria  

**Descripción:** Permite ingresar un nuevo paciente al sistema con sus datos personales.

**Flujo principal de eventos:**
1. Secretaria Valeria accede a “Registrar paciente”.
2. El sistema muestra un formulario.
3. Ingresa nombre, DNI y contacto (Ej: Juan Pérez, DNI 12345678).
4. Confirma el registro.
5. El sistema valida los datos.
6. El sistema guarda el paciente y muestra confirmación.

**Precondiciones:**
- Usuario autenticado.

**Postcondiciones:**
- Paciente registrado correctamente.

---

## Caso de Uso 2: Registrar médico

**Actor(es):** Administrador  

**Descripción:** Permite registrar un médico con su especialidad y horarios.

**Flujo principal de eventos:**
1. El administrador accede a “Registrar médico”.
2. El sistema muestra el formulario.
3. Ingresa datos (Ej: Dr. Molina, Clínica Médica, lunes a viernes 9 a 17 hs).
4. Confirma la operación.
5. El sistema valida la información.
6. El sistema guarda el médico.

**Precondiciones:**
- Usuario con permisos de administrador.

**Postcondiciones:**
- Médico registrado en el sistema.

---

## Caso de Uso 3: Agendar turno

**Actor(es):** Secretaria Valeria  

**Descripción:** Permite asignar un turno a un paciente con el Dr. Molina.

**Flujo principal de eventos:**
1. Secretaria Valeria selecciona “Agendar turno”.
2. El sistema solicita paciente y médico.
3. Selecciona paciente (Ej: Juan Pérez).
4. Selecciona médico: Dr. Molina.
5. Elige fecha y hora disponible (Ej: 10/04/2026 - 10:00 hs).
6. El sistema verifica disponibilidad.
7. Confirma el turno.
8. El sistema registra el turno y muestra confirmación.

**Precondiciones:**
- Paciente y médico registrados.
- Disponibilidad horaria.

**Postcondiciones:**
- Turno asignado correctamente.

---

## Caso de Uso 4: Cancelar turno

**Actor(es):** Secretaria Valeria / Paciente  

**Descripción:** Permite cancelar un turno existente.

**Flujo principal de eventos:**
1. Secretaria Valeria accede a “Cancelar turno”.
2. El sistema muestra turnos.
3. Selecciona turno (Ej: Juan Pérez - Dr. Molina - 10/04/2026).
4. El sistema pide confirmación.
5. Confirma cancelación.
6. El sistema elimina o marca el turno como cancelado.
7. Se muestra mensaje de confirmación.

**Precondiciones:**
- Existencia de turnos.

**Postcondiciones:**
- Turno cancelado y horario disponible.

---

## Caso de Uso 5: Consultar turnos

**Actor(es):** Secretaria Valeria  

**Descripción:** Permite visualizar turnos según distintos criterios.

**Flujo principal de eventos:**
1. Accede a “Consultar turnos”.
2. El sistema muestra opciones de búsqueda.
3. Selecciona criterio (Ej: por médico Dr. Molina).
4. El sistema procesa la consulta.
5. Muestra lista de turnos.
6. Secretaria Valeria revisa la información.

**Precondiciones:**
- Turnos registrados.

**Postcondiciones:**
- Información mostrada correctamente.
---

## Boceto inicial del diseño de clases

### Clases identificadas

- Paciente (nombre, DNI, teléfono)
- Médico (nombre, especialidad)
- Turno (fecha, hora)
- Recepcionista

### Relaciones

- Un paciente puede tener varios turnos  
- Un médico puede atender varios turnos  
- Un turno pertenece a un paciente y a un médico.