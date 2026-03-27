### Anexo - Introducción al Diseño Orientado a Objetos
El diseño orientado a objetos es un enfoque conceptual que organiza el software como una colección de objetos que contienen tanto datos como comportamientos, este paradigma se centra en modelar objetos del mundo real o simulados, dividiendo el sistema en unidades independientes.
# Los cuatro fundamentos de POO
- Encapsulación: Protege los datos restringiendo el acceso, se realiza exclusivamente a través de interfaces públicas o métodos, que promuevan la seguridad y modularidad.
- Herencia: Premite crear una clase nueva a partir de una clase base, heredando sus atributos y comportamientos.
- Polimorfismo: Es la capacidad que tienen diferentes objetos en una jerarquía de clases para responder de manera distinta a un mismo mensaje o comando.
- Abstracción: Es el proceso de simplificar lo complejo, ocultando detalles innecesarios para el usuario.
# Introducción

## ¿Qué es la Programación Orientada a Objetos?

La Programación Orientada a Objetos (POO) es un paradigma de programación que organiza el software en objetos. Estos objetos representan entidades del mundo real y contienen datos (atributos) y comportamientos (métodos). Este enfoque permite desarrollar sistemas más organizados, reutilizables y fáciles de mantener.

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

- RF1: El sistema debe permitir registrar pacientes con sus datos personales.
- RF2: El sistema debe permitir registrar médicos con su especialidad.
- RF3: El sistema debe permitir asignar turnos a pacientes.
- RF4: El sistema debe permitir cancelar turnos existentes.
- RF5: El sistema debe permitir consultar los turnos disponibles.

### Requisitos no funcionales

- RNF1: El sistema debe ser fácil de usar para el personal administrativo.
- RNF2: El sistema debe estar disponible las 24 horas del día.
- RNF3: El sistema debe garantizar la seguridad de los datos.
- RNF4: El sistema debe tener un tiempo de respuesta rápido.
- RNF5: El sistema debe ser escalable para agregar nuevas funcionalidades.

---

## Casos de uso

### Caso de uso 1: Registrar paciente

- Actor: Recepcionista  
- Descripción: Permite registrar un nuevo paciente en el sistema.  
- Flujo principal:
  1. El recepcionista accede al sistema
  2. Selecciona la opción “Registrar paciente”
  3. Ingresa los datos del paciente
  4. Confirma la información
  5. El sistema guarda los datos  
- Precondición: El sistema está en funcionamiento  
- Postcondición: El paciente queda registrado en el sistema  

---

### Caso de uso 2: Registrar médico

- Actor: Administrador  
- Descripción: Permite registrar un nuevo médico en el sistema.  
- Flujo principal:
  1. El administrador accede al sistema
  2. Selecciona “Registrar médico”
  3. Ingresa los datos del médico
  4. Confirma la información
  5. El sistema guarda los datos  
- Precondición: Usuario autenticado  
- Postcondición: Médico registrado  

---

### Caso de uso 3: Asignar turno

- Actor: Recepcionista  
- Descripción: Permite asignar un turno a un paciente.  
- Flujo principal:
  1. El recepcionista selecciona un paciente
  2. Selecciona fecha y hora
  3. Selecciona un médico
  4. Confirma el turno
  5. El sistema guarda la información  
- Precondición: Paciente registrado  
- Postcondición: Turno asignado correctamente  

---

### Caso de uso 4: Cancelar turno

- Actor: Recepcionista  
- Descripción: Permite cancelar un turno existente.  
- Flujo principal:
  1. El recepcionista busca el turno
  2. Selecciona la opción cancelar
  3. Confirma la acción
  4. El sistema elimina el turno
  5. El sistema notifica la cancelación  
- Precondición: Turno existente  
- Postcondición: Turno eliminado  

---

### Caso de uso 5: Consultar turnos

- Actor: Recepcionista  
- Descripción: Permite visualizar los turnos disponibles.  
- Flujo principal:
  1. El usuario accede al sistema
  2. Selecciona la opción consultar turnos
  3. El sistema muestra la lista
  4. El usuario filtra resultados
  5. Visualiza la información  
- Precondición: Sistema activo  
- Postcondición: Información mostrada en pantalla  

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
- Un turno pertenece a un paciente y a un médico
