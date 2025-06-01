
# **Nombre del Proceso:**  
## Creación de cita

---

## **Objetivo**  
Registrar nuevas citas en el sistema asignando paciente, terapeuta, sala y horario disponible, validando que no existan conflictos con agendas existentes.

---

## **Actores**  
- **Secretaria:** Ingresa los datos de la nueva cita y asigna recursos.
- **Sistema:** Valida disponibilidad y aplica reglas de negocio.

---

## **Entradas**  

- Paciente registrado (nombre)
- Tipo de servicio (evaluación inicial o terapia)
- Terapeuta disponible
- Fecha y hora de inicio
- Sala asignada
- Comprobante de pago (para terapias)

---

## **Pasos**  
1. **Acceso al Módulo de Agenda:**  
   La Secretaria inicia sesión en el sistema y accede al módulo de gestión de agenda.  
2. **Acceso al formulario:**  
   La secretaria hace clic en "Nuevo Evento" desde la vista de agenda.  
3. **Ingreso de Datos Personales:**  
   La secretaria completa el formulario con los datos requeridos de la cita, como paciente (ya creado), terapeuta asignado, fecha y hora de inicio, sala de la cota, comporbante de pago y cuota a pagar.  
4. **Guardado de cita:**  
   La Secretaria guarda la información de la cita en el formulario.
5. **Validación automatica:**  
   El sistema comprueba que la cita a crear no sea en fin de semana y no este sobrepuesta a otras citas.  
6. **Confirmación:**  
   Guarda la cita y actualiza la vista de agenda.
   
---

## **Excepciones**  
- **Datos Incompletos o Erróneos:**  
  Si algún campo obligatorio no está lleno o contiene información inválida, el sistema no bloqueará el guardado y mostrará un mensaje de error indicando los elementos faltante o erroneo.  
- **Sala no disponible:**
  Si la sala esta ocupada en la hora que se busca guardar, el sistema bloqueará el guardado y mostrara un mensaje de error indicando que la sala esta ocupada en dicho rango de horario.
- **Terapeuta no disponible:**
  Si el terapeuta esta ocupado a la hora en la quw se busca realizar la cita, el sistema bloqueará el guardado y mostrara un mensaje de error indicando que la sala esta ocupada en dicho rango de horario.
- **Falta de comprobante de pago:**
  Si se elige el evento cia de terapia y no se sube comprobante de pago, el sistema no permitirá continuar y mostrara un mensaje indicando la documentación faltante.
---

## **Resultados Esperados**  

- Nueva cita registrada en la agenda con todos los datos requeridos.
- Actualización en tiempo real de la disponibilidad de recursos.
- Generación automática de folio único (una ves se asigna el paciente).

---

## **Notas Adicionales**  
- Las evaluaciones iniciales tienen prioridad en la asignación de horarios.
- El comporobante de pago debe ser en formato JPEG, PNG o PDF, de maximo 5 MB.

---

##

# **Nombre del Proceso:**  
## Reprogamación de cita

---

## **Objetivo**  
Modificar fecha, hora o recursos asignados a una cita existente, manteniendo la integridad de las agendas involucradas.

---

## **Actores**  
- **Secretaria:** Ejecuta el cambio desde la bandeja de reprogramaciones o directamente en la agenda.
- **Paciente:** Puede solicitar reprogramación (pendiente de aprobación).

---

## **Entradas**  
- Cita existente a modificar
- Nueva fecha/hora propuesta
- Justificación del cambio (opcional)
- Disponibilidad actualizada de terapeutas/salas

---

## **Pasos**  

1. **Acceso al Módulo de Agenda:**  
   La Secretaria inicia sesión en el sistema y accede al módulo de gestión de agenda.  
2. **Acceso al cita a reprogramar:**  
   La secretaria accede a la cita a reprogramar de cualquiera de las 2 maneras:
     En la pestaña de reprogramaciones en la bandeja de entrada y dando click en gestionar.
     Seleccionando la cita desde la agenda y dando click en reprogramar.  
5. **Modificación de datos:**  
   La secretaria cambia los parametros editables necesarios: hora, fecha y terapeuta asignado.  
6. **Guardado de cita:**  
   La Secretaria guarda la cita con la información modificada en el formulario.
7. **Validación automatica:**  
   El sistema comprueba que la cita a reprogramada no sea en fin de semana y no este sobrepuesta a otras citas. 
8. **Confirmación:**  
   Se guarda la cita y actualiza la vista de agenda.
   
---

## **Excepciones**  
- **Datos Incompletos o Erróneos:**  
  Si algún campo obligatorio no está lleno o contiene información inválida, el sistema no bloqueará el guardado y mostrará un mensaje de error indicando los elementos faltante o erroneo.  
- **Sala no disponible:**
  Si la sala esta ocupada en la hora que se busca guardar, el sistema bloqueará el guardado y mostrara un mensaje de error indicando que la sala esta ocupada en dicho rango de horario.
- **Terapeuta no disponible:**
  Si el terapeuta esta ocupado a la hora en la quw se busca realizar la cita, el sistema bloqueará el guardado y mostrara un mensaje de error indicando que la sala esta ocupada en dicho rango de horario.
- **Cita no encontrada:**
  Si no se encuentra el evento original para reprogramar, el sistema no permitura desplegar el formuilario y mostrará un mensaje de error indicando que no se encontró el evento original para reprogramar.
---

## **Resultados Esperados**  
- Liberación automática del horario anterior.
- Cita actualizada en el sistema con nuevos parámetros.
- Visualización de la cita reprogramada en la agenda.

---

## **Notas Adicionales**  
- El sistema mantiene el folio original durante la reprogramación.

---

##

# **Nombre del Proceso:**  
## Gestión de solicitudes

---

## **Objetivo**  
Procesar solicitudes pendientes de nuevas citas recibidas a través de la bandeja de entrada del sistema.

---

## **Actores**  
- **Secretaria:** Revisa, modifica y rechaza solicitudes de cita.
- **Sistema:** Clasifica automáticamente las solicitudes por tipo.

---

## **Entradas**  
- Solicitudes de nuevas citas (con nombre del paciente, tipo de evento y fecha propuesta)
- Disponibilidad actual de la agenda

---

## **Pasos**  

1. **Acceso al Módulo de Agenda:**  
   La Secretaria inicia sesión en el sistema y accede al módulo de gestión de agenda.  
2. **Acceso a la solicitud:**  
   La secretaria accede a la cita a solicitud en la pestaña de solicitudes en la bandeja de entrada y dando click en gestionar.
3. **Evaluación de solicitud:**  
   La secretaria evalua la solicitud y analiza la disponibilidad en la agenda.
4. **Guardado de cita:**  
   La Secretaria guarda la cita solicitada (con modificaciones pertinentes si es necesario).
5. **Validación automatica:**  
   El sistema comprueba que la cita programada no sea en fin de semana y no este sobrepuesta a otras citas. 
6. **Confirmación:**  
   Se guarda la cita y actualiza la vista de agenda.
   
---

## **Excepciones**  
- **Datos Incompletos o Erróneos:**  
  Si algún campo obligatorio no está lleno o contiene información inválida, el sistema no bloqueará el guardado y mostrará un mensaje de error indicando los elementos faltante o erroneo.  
- **Sala no disponible:**
  Si la sala esta ocupada en la hora que se busca guardar, el sistema bloqueará el guardado y mostrara un mensaje de error indicando que la sala esta ocupada en dicho rango de horario.
- **Terapeuta no disponible:**
  Si el terapeuta esta ocupado a la hora en la quw se busca realizar la cita, el sistema bloqueará el guardado y mostrara un mensaje de error indicando que la sala esta ocupada en dicho rango de horario.
- **Cita no encontrada:**
  Si no se encuentra el evento original para reprogramar, el sistema no permitura desplegar el formuilario y mostrará un mensaje de error indicando que no se encontró el evento original para reprogramar.
---

## **Resultados Esperados**  
- Cita creada con los parametros de la solicitud (si es posible).
- Visualización de la cita reprogramada en la agenda.

---

## **Notas Adicionales**  
- Las solicitudes tienen caducidad (7 días sin atender se archivan automáticamente).
- Prioridad automática para evaluaciones iniciales sobre terapias.

---

##

# **Nombre del Proceso:**  
## Visualización de agenda

---

## **Objetivo**  
Consultar las citas programadas mediante diferentes vistas (diaria/semanal) y filtros para facilitar la gestión del flujo clínico.

---

## **Actores**  
- Secretaria: Navega por la agenda según necesidades operativas.
- **Sistema:** Desplega la visualización de las citas y asegura que no hayan solpamientos entre estas (ya sea de sala o terapeuta).
- **Coordinadora:** Supervisa la distribución de citas y resuelve conflictos complejos en la agenda.
- 
---

## **Entradas** 

- Periodo de tiempo para la visualización en la agenda (dia/semana)
- Fecha especifica
- citas agendadas (almacenadas en la base de datos)

---

## **Pasos**  

1. **Acceso al Módulo de Agenda:**  
   La Secretaria inicia sesión en el sistema y accede al módulo de gestión de agenda, en horarios disponibles desde la pagina principal.  
2. **Selección de vista:**  
   La secretaria elige entre vista diaria (1 columna vertical por dia) o vista semanal (5 columnas verticales, para lunes-viernes)
3. **Navegación temporal:**  
   La secretaria usa calendario embebido para saltar a una fecha específica.
4. **Consulta de agenda:**  
   La Secretaria evalua las citas por dia segun el color de la cabecera de la columna, y los recuadros dentro de cada hora de la agenda.
5. **Consulta de cita:**  
   La secretaria ingresa a una cita especifica para ver su información relacionada como tipo de cita, paciente, folio, fecha, hora de inicio, duración, sala, terapeuta y comporbante. 

---

## **Excepciones**  
- **Sobrecarga de citas:**  
  Cabeceras en rojo activan alerta para redistribución de carga.

---

## **Resultados Esperados**  
- Visualización clara e intuitiva de la programación clínica.
- Capacidad para identificar rápidamente disponibilidades.
- Acceso inmediato a detalles operativos de cada cita.

---

## **Notas Adicionales**  
-Las citas estan codificadas por color, siendo morado usado para evaluaciones iniciales y azul para cita de terapia.
-Las cabeceras de la agenda (correspondientes al dia) estan codificadas por color, siendo verde una ocupación de <25%, amarillo 25%-75% y rojo un <75%.
- La vista semanal excluye fines de semana (no hay atención).
- Click en slot vacío abre directamente formulario para nueva cita.
- Compatible con impresión en formato optimizado (botón "Imprimir").
- 
---
