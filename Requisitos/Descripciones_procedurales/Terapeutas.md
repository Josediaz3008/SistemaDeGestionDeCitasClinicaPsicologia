# **Nombre del Proceso:**  
## Creación del Terapeuta

---

## **Objetivo**    
Registrar a nuevos terapeutas en el sistema de gestión de citas clínicas, asegurando que sus datos personales, credenciales, especialidad y disponibilidad inicial estén correctamente configurados para su incorporación a la agenda institucional.

---

## **Actores**  
- **Secretaria:** Encargada de ingresar los datos del nuevo terapeuta, asignar su disponibilidad preliminar y vincularlo con el módulo de agenda.  
- **Coordinadora:** Verifica la validez de los datos registrados, aprueba la activación del perfil del terapeuta y supervisa la correcta integración en la programación clínica.

---

## **Entradas**  
- Datos personales del terapeuta (nombre, documento, correo, número de contacto)  
- Especialidad y tipo de atención que brindará (psicoterapia individual, grupal, etc.)  
- Disponibilidad horaria preliminar  
- Información académica o profesional (título, número de cédula profesional, si aplica)  
- Unidad o facultad asignada

---

## **Pasos**  
1. **Acceso al Módulo de Terapeutas:**  
   La Secretaria inicia sesión en el sistema y accede al módulo de gestión de terapeutas.  
2. **Selección de “Nuevo Terapeuta”:**  
   Hace clic en la opción “Registrar nuevo terapeuta” en la interfaz del sistema.  
3. **Ingreso de Datos Personales y Profesionales:**  
   Completa el formulario con los datos requeridos del terapeuta, como nombre completo, correo institucional, especialidad, facultad y nivel de atención.  
4. **Configuración de Disponibilidad Inicial:**  
   Define la disponibilidad semanal del terapeuta, indicando los días y horas en los que podrá recibir pacientes.  
5. **Guardar Registro:**  
   La Secretaria guarda la información y el sistema crea el nuevo perfil del terapeuta.

---

## **Excepciones**  
- **Datos Incompletos o Erróneos:**  
  Si algún campo obligatorio no está lleno o contiene información inválida, el sistema no permitirá continuar y mostrará un mensaje de error.  
- **Duplicación de Terapeuta:**  
  Si se detecta que el terapeuta ya está registrado (por ejemplo, por correo electrónico o número de documento), se emite una advertencia y se impide la creación duplicada.

---

## **Resultados Esperados**  
- El terapeuta queda correctamente registrado en el sistema, con su disponibilidad inicial activa.  
- Su perfil aparece en la lista de terapeutas disponibles para la programación de citas.  
- Se garantiza la trazabilidad de la creación, indicando fecha, hora y usuario que realizó el registro.

---

## **Notas Adicionales**  
- Se recomienda que la Coordinadora revise periódicamente los registros nuevos para asegurar su correcta integración.  
- El sistema debe contar con validaciones en tiempo real para evitar errores comunes en la captura de datos.  

---

##
# **Nombre del Proceso:**  
## Modificación de datos del Terapeuta

---

## **Objetivo**  
Controlar y actualizar en tiempo real la disponibilidad de los terapeutas, permitiendo la identificación de posibles conflictos o ausencias y facilitando la toma de decisiones para optimizar la programación de citas.

---

## **Actores**  
- **Secretaria:** Realiza la revisión periódica y la actualización de la disponibilidad de los terapeutas en el sistema, utilizando la interfaz de gestión de agendas.  
- **Coordinadora:** Supervisa el proceso, valida los cambios y toma decisiones en situaciones excepcionales, como ausencias prolongadas o cambios imprevistos en la agenda.

---

## **Entradas**  
- Registro actualizado de la agenda de terapias y citas  
- Información personal y de disponibilidad asignada a cada terapeuta  
- Notificaciones o alertas de incidencias en los horarios programados  
- Información de cambios o solicitudes de ajuste provenientes de los terapeutas o del personal administrativo

---

## **Pasos**  
1. **Acceso a la Sección de Terapeutas:** La Secretaria inicia sesión en el sistema y navega hacia el módulo de “Terapeutas”.  
2. **Visualización de la Agenda de Terapeutas:** Se despliega un listado de los terapeutas indicando sus datos personales, horarios, etc.  
3. **Selección y Revisión:** La Secretaria selecciona un terapeuta específico para revisar su calendario, verificando que los horarios disponibles y los asignados sean correctos y no presenten conflictos.  
4. **Actualización del Estado:** La Secretaria procede a actualizar el estado o información deseado del terapeuta.  
5. **Registro de Cambios:** El sistema registra en un historial la modificación realizada, incluyendo la fecha, hora y el usuario (la Secretaria o, en casos de intervención, Coordinadora) que efectuó el cambio.  
6. **Supervisión y Validación:** La Coordinadora revisa periódicamente los cambios y recibe notificaciones de cualquier incidencia para confirmar que la disponibilidad reflejada es correcta y está alineada con la realidad del servicio.

---

## **Excepciones**  
- **Conflicto en la Agenda:**  
  Si se detecta que dos citas se han superpuesto o que un terapeuta figura como disponible mientras tiene asignado un bloqueo, el sistema envía una alerta inmediata. La Secretaria debe corregir el conflicto manualmente o notificar a Coordinadora para tomar una decisión conjunta.  

- **Error de Sincronización de Datos:**  
  En caso de que la actualización en tiempo real falle (por ejemplo, por problemas de conexión o error del servidor), se solicita al usuario refrescar la pantalla; si el problema persiste, se debe notificar al área de soporte para restablecer la comunicación.  

- **Inconsistencia en los Datos de Disponibilidad:**  
  Si la información del terapeuta no coincide con la realidad (por ejemplo, el terapeuta reporta una ausencia no reflejada en el sistema), se debe proceder a una actualización manual y registrar la incidencia en el historial para futuras auditorías.

---

## **Resultados Esperados**  
La disponibilidad de los terapeutas se refleja correctamente en la agenda del sistema, sin conflictos ni inconsistencias. Todas las modificaciones quedan registradas en el historial y se notifican oportunamente las incidencias a los responsables, garantizando así la correcta gestión de citas.

---

## **Notas Adicionales**  
Es recomendable realizar revisiones periódicas por parte de la Coordinadora para garantizar que los datos reflejados en el sistema estén siempre alineados con la realidad operativa.  

---

##
# **Nombre del Proceso:**  
## Consulta de la información del terapeuta

---

## **Objetivo**   
_Consultar la información de un terapeuta en específico, ya sea mediante selección o búsqueda manual._

---

## **Actores**  
- **Secretaria:** Ejecuta la consulta de un terapeuta manualmente o mediante búsqueda.

---

## **Entradas**  
- En caso de ser mediante búsqueda por filtros:  
  - Nombre del terapeuta  
  - Rol del terapeuta  
  - Tipo de servicio  
- En caso de ser búsqueda manual (mediante clickeando en la lista), no necesita entradas.

---

## **Pasos**  

**En caso de búsqueda:**  
1. **Acceso al sistema:** La secretaría entra al sistema de gestión de sistemas y da click en “Ir a Agenda”.  
2. **Acceso a sección de terapeutas:** La secretaria entra a la sección de terapeutas de la barra de navegación, donde se desplegará una sección de búsqueda por filtros.  
3. **Ingreso de filtros:** La secretaria ingresa los datos del terapeuta a consultar en los filtros de búsqueda (nombre, rol y tipo).  
4. **Ejecución de búsqueda:** La secretaria ejecuta la búsqueda y la lista se actualizará mostrando al terapeuta que cumple con los criterios de búsqueda.  
5. **Consulta:** La secretaría hace click en el nombre del terapeuta y se mostrará la información del terapeuta como pacientes asignados, email, rol, tipo, servicio y horarios de disponibilidad.  

**En caso de búsqueda manual (terapeuta aparece en la lista):**  
1. **Acceso al sistema:** La secretaría entra al sistema de gestión de sistemas y da click en “Ir a Agenda”.  
2. **Acceso a sección de terapeutas:** La secretaria entra a la sección de terapeutas de la barra de navegación, donde se desplegará un lista de terapeutas.  
3. **Consulta:** La secretaría hace click en el nombre del terapeuta y se mostrará la información del terapeuta como pacientes asignados, email, rol, tipo, servicio y horarios de disponibilidad.

---

## **Excepciones**  
**Ausencia de coincidencias:**  
La búsqueda ejecutada mediante filtros no genera ninguna coincidencia o la coincidencia no es la deseada, en estos casos la secretaría deberá corroborar que los datos ingresados sean correctos o que existe un terapeuta con los datos ingresados.

---

## **Resultados Esperados**  
- En caso de ejecutar una búsqueda por filtros, la búsqueda deberá proporcionar al terapeuta según los datos ingresados y desplegar sus datos al hacer click.  
- En caso de hacer una búsqueda manual, al hacer click en el terapeuta, se deberán desplegar los datos del mismo.

---

## **Notas Adicionales**  
_Ninguna._

---
