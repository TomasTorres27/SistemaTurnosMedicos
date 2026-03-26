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