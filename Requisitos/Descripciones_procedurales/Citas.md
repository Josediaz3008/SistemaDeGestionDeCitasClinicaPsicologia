# **Nombre del Proceso:**  
## Cancelación de Citas

---

## **Objetivo**  
_Cancelar de manera oportuna y organizada las citas previamente agendadas cuando se notifica la imposibilidad de asistencia._

---

## **Actores**  
- **Secretaria:** Identifica y ejecuta la cancelación de la cita cuando se confirma que el paciente no asistirá.  
- **Coordinadora:** Supervisa el proceso y puede intervenir en situaciones excepcionales que requieran ajustes o confirmación adicional.

---

## **Entradas**  
- Registro de la cita a cancelar.  
- Confirmación de la no asistencia enviada previamente por el paciente con 24 horas de antelación.  
- Filtros de búsqueda (fecha, nombre o servicio) para identificar la cita en cuestión.

---

## **Pasos**  
1. **Identificación de la Cita:**  
   La Secretaria accede a la sección de gestión de citas y utiliza los filtros para localizar la cita que debe ser cancelada por no asistencia.
2. **Selección del Registro:**  
   Se selecciona la cita a cancelar y se verifica el estado actual de la misma.
3. **Ejecución de la Cancelación:**  
   La Secretaria activa la opción de “Cancelar Cita”, y el sistema actualiza inmediatamente el registro a “cancelada”.
4. **Registro de la Acción:**  
   El sistema anota la acción de cancelación en el historial para efectos de seguimiento. Se marca como “no asistida” y se despliega una sección donde se escribe quién canceló la cita y el motivo de la cancelación.
5. **Actualización de la Agenda:**  
   La agenda se actualiza en tiempo real, eliminando la cita cancelada de la visualización activa.
6. **Notificación Interna:**  
   Se notifica internamente a la Coordinadora acerca de la cancelación realizada para control y supervisión del proceso.

---

## **Excepciones**  
- **Error en la Selección de Registro:**  
  Si no se logra identificar correctamente la cita o se detecta que el estado no corresponde a “no asistencia”, el sistema emite una alerta para que la Secretaria verifique manualmente el registro.
- **Fallo en la Actualización de la Agenda:**  
  En caso de error al actualizar la visualización de la agenda, se notifica a la Coordinadora para solucionar la incidencia de inmediato.
- **Falla en el Registro del Historial:**  
  Si el sistema falla al registrar la cancelación en el historial, se debe proceder a un registro manual suplementario y se informa la situación para revisión posterior.

---

## **Resultados Esperados**  
_La cita se cancela de forma correcta en el sistema, la agenda se actualiza en tiempo real y el cambio queda debidamente registrado en el historial junto con el detalle de motivos adicionales._

---

## **Notas Adicionales**  
- En el caso de que durante todo el proceso de terapia se registren 3 faltas injustificadas o 5 cancelaciones, se dará por cancelado el proceso terapéutico.  
- Si el terapeuta cancela, se avisa al paciente con tiempo. Si hay disponibilidad, se reagenda esa semana; si no, se continúa en la próxima sesión, pero el proceso se extiende para recuperar la cita perdida.  
- Si el paciente cancela, no se recupera la sesión, a menos que justifique su ausencia con documentos (como receta médica o motivo grave). En ese caso, debe enviar el comprobante al área de coordinación para evaluar extender el proceso.  
- Se recomienda mantener una comunicación clara con el paciente para coordinar la reprogramación, preferentemente

---

##
# **Nombre del Proceso:**  
## Reprogramación de cita ante inasistencia

---

## **Objetivo**  
_Reprogramar de manera eficiente las citas en las que el paciente no asistió, asegurando la continuidad en la atención y dejando constancia en el historial para facilitar el seguimiento._

---

## **Actores**  
- **Secretaria:** Ejecuta el proceso de identificación y reprogramación de la cita no asistida.  
- **Coordinadora:** Supervisa el proceso y, en algunos casos, autoriza la reprogramación o interviene en situaciones de excepción.

---

## **Entradas**  
- Registro de la cita marcada como “no asistida”.  
- Filtros de búsqueda (fecha, nombre del paciente o servicio) para identificar la cita.  
- Nueva fecha y hora propuestas para la reprogramación.  
- Datos de contacto del paciente (número telefónico).

---

## **Pasos**  
1. **Búsqueda de la Cita:**  
   La Secretaria ingresa a la sección de gestión de citas y utiliza los filtros disponibles (por fecha, nombre o servicio) para localizar la cita y marcarla como “no asistida”.  
2. **Selección de Reprogramación:**  
   Una vez identificada, se selecciona la opción “Reprogramar cita” y se despliega una interfaz para la nueva fecha y hora.  
3. **Ingreso de Nueva Fecha y Hora:**  
   La Secretaria introduce la nueva fecha y hora disponibles para la reprogramación, verificando la disponibilidad de terapeutas y consultorios.  
4. **Registro en el Historial:**  
   El sistema actualiza la agenda y almacena en el historial el cambio de programación, registrando la acción y el usuario que realizó el cambio.  
5. **Notificación al Paciente:**  
   Se registra la notificación a realizar vía llamada telefónica (se incluye opcionalmente el envío de SMS en el futuro) para informar al paciente de la nueva cita.  
6. **Verificación y Cierre:**  
   Finalmente, se actualizan los indicadores del sistema y se muestra un mensaje de confirmación a la Secretaria.

---

## **Excepciones**  
- **Nueva Fecha No Disponible:**  
  Si la fecha o el horario seleccionado no se encuentran disponibles, el sistema informa al usuario y solicita elegir otra opción. La solicitud queda en espera hasta que se disponga de una nueva fecha válida.  
- **Error en la Actualización del Historial:**  
  En caso de falla al registrar el cambio en el historial, se notifica inmediatamente a la Coordinadora para intervenir y corregir el registro manualmente.  
- **Fallo en la Notificación:**  
  Si se presenta algún inconveniente en el proceso de notificación (por ejemplo, error en la integración con el sistema telefónico o SMS), se activa un procedimiento alternativo para notificar al paciente vía llamada directa y se registra la incidencia.

---

## **Resultados Esperados**  
_La cita inicialmente marcada como “no asistida” se reprograma correctamente, se actualiza la agenda en tiempo real, se registra el historial de cambio y se notifica al paciente vía llamada telefónica._

---

## **Notas Adicionales**  
- La notificación primaria se realiza mediante llamada telefónica, aunque se contempla la incorporación de SMS como mecanismo complementario.  
- Si el terapeuta cancela, se avisa al paciente con tiempo. Si hay disponibilidad, se reagenda esa semana; si no, se continúa en la próxima sesión, pero el proceso se extiende para recuperar la cita perdida.  
- Si el paciente cancela, no se recupera la sesión, a menos que justifique su ausencia con documentos (como receta médica o motivo grave). En ese caso, debe enviar el comprobante al área de coordinación para evaluar extender el proceso.  
- El registro histórico es clave para el seguimiento y la posterior auditoría de cambios en la agenda.

---

##
# **Nombre del Proceso:**  
## Cancelación del Servicio

---

## **Objetivo**    
_Registra y ejecuta la cancelación definitiva del tratamiento para pacientes que han dejado de asistir o han decidido cancelar la terapia, garantizando que el proceso se documente, se actualice la agenda y se coordine la transición a servicios externos o el cierre del expediente._

---

## **Actores**  
- **Coordinadora:** Ejecuta el proceso de cancelación, actualiza la agenda y notifica internamente los cambios. Valida la cancelación y coordina el traslado a servicios externos o el cierre del expediente según la causa de la cancelación.

---

## **Entradas**  
- Registro de la cita o tratamiento activo que se desea cancelar.  
- Notificación de cancelación recibida por el paciente (por falta de asistencia prolongada, decisión propia o indicación de canalización a otra clínica).  
- Información de contacto y datos relevantes del paciente para la verificación del caso.  
- (Opcional) Solicitud formal o comunicación externa que respalde la cancelación, en caso de canalización a otra clínica.

---

## **Pasos**  
1. **Verificación de Solicitud:**  
   La coordinadora recibe la notificación de cancelación, ya sea por comunicación telefónica directa del paciente o por aviso de no asistencia prolongada. Se revisa el registro del paciente en el sistema para confirmar que el tratamiento está activo.  
2. **Acceso al Registro de Tratamiento:**  
   Se localiza el expediente o el registro de la cita/tratamiento en el sistema utilizando los filtros disponibles (por nombre, cédula o número de expediente).  
3. **Selección de Opción de Cancelación:**  
   La coordinadora selecciona la opción “Cancelar Servicio” en el menú de gestión de citas/tratamientos.  
4. **Ingreso de Motivo y Observaciones:**  
   Se ingresan las observaciones pertinentes que justifiquen la cancelación, especificando si se trata de una solicitud del paciente, una indicación de canalización a una clínica externa u otra razón.  
5. **Actualización de la Agenda y Expediente:**  
   El sistema actualiza el estado del tratamiento a “Cancelado” y elimina o marca la cita de forma definitiva para no considerarla en la programación futura.  
6. **Notificación Interna y Coordinación:**  
   Se notifica a la coordinadora sobre la cancelación del servicio. En casos de canalización externa, se coordina el traspaso del expediente y se informa a los departamentos correspondientes.  
7. **Registro Histórico:**  
   Se guarda un registro en el historial de cambios del paciente, con fecha, hora, motivo y usuario que realizó la cancelación, para futuras auditorías y seguimiento.  
8. **Cierre del Proceso:**  
   Se confirma en el sistema la cancelación y se despliega un mensaje de confirmación. Se coordina, si es necesario, la realización de una llamada de seguimiento con el paciente para confirmar la decisión.

---

## **Excepciones**  
- **Solicitud de Cancelación No Encontrada o Incongruente:**  
  Si el sistema no localiza el registro activo del tratamiento o el estado no permite la cancelación (por ejemplo, si ya se encuentra cancelado), se muestra un mensaje de error solicitando la verificación manual del expediente.  
- **Error en la Actualización de la Agenda:**  
  En el caso de que la actualización del estado del tratamiento falle, el sistema muestra un mensaje de error y se debe notificar a la coordinadora para intervenir y realizar la actualización de forma manual.  
- **Falta de Justificación Detallada:**  
  Si al ingresar la cancelación no se proporciona un motivo claro u observaciones justificativas, el sistema rechaza temporalmente el cambio y solicita completar dichos campos antes de proceder.  
- **Problemas en la Coordinación Externa:**  
  En casos de canalización a una clínica externa, si los datos de contacto o la comunicación con la clínica fallan, se deberá intentar nuevamente la coordinación y registrar el intento para seguimiento posterior.

---

## **Resultados Esperados**  
_El tratamiento se cancela de forma definitiva en el sistema, la agenda se actualiza para reflejar la eliminación de la cita activa y se documenta de forma detallada el motivo de cancelación, permitiendo una transición ordenada ya sea al cierre del expediente o a la canalización a otra clínica._

---

## **Notas Adicionales**  
- Es fundamental mantener una comunicación directa y clara con el paciente para confirmar la decisión de cancelar el servicio.  
- El registro histórico permite el análisis de tendencias en cancelaciones, lo que puede ser útil para implementar medidas de mejora en la adherencia terapéutica.  
- Se recomienda que la coordinadora coordine reuniones periódicas para revisar los casos de cancelación y evaluar las posibles necesidades de ajuste en los protocolos de atención.
