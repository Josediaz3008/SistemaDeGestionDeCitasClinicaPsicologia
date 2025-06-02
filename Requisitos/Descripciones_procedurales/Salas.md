# **Nombre del Proceso**  
## Administración de Salas / Consultorios (Prototipo – sin backend)

---

## **Objetivo**  
Permitir a la **Coordinadora** (o Administrador) **crear, editar, bloquear/liberar y eliminar** consultorios dentro de la interfaz del prototipo para que el equipo valide flujos de agenda y distribución de servicios **sin** necesidad de un servidor ni base de datos real.

> **Persistencia simulada**  
> Toda la información se guarda en `localStorage` o en variables en memoria. Se pierde al borrar caché o hacer “Hard Reload”.

---

## **Actores**  

| Actor           | Permisos en la UI                  | Observaciones                         |
|-----------------|------------------------------------|---------------------------------------|
| **Coordinadora**| Alta, edición, bloqueo/liberación y eliminación visual. | Acceso completo a los botones de la tabla. |
| **Administrador** | Mismos permisos que la Coordinadora.| Diferencia únicamente en la etiqueta/rol. |
| **Secretaria / Becaria** | Solo lectura. | En el prototipo se emula ocultando los botones de acción. |

---

## **Entradas (Formulario/Módal)**  

- **Nombre** del consultorio (único).  
- **Servicios** que atiende (checkbox — debe seleccionarse al menos uno).  
- **Horario de operación**:  
  - **Hora Inicio** y **Hora Fin** dentro del rango **09 h – 18 h**.  
  - Fin debe ser posterior al inicio.  

---

## **Flujo UI (prototipo)**  

### 1. Ver listado  
La Coordinadora ingresa a **Salas** desde la barra de navegación y revisa la tabla actual (datos cargados desde `localStorage.salas[]`).

### 2. Crear  
| Paso | Descripción |
|------|-------------|
| 2.1 | `click` **«Agregar Sala»**. Se muestra un modal vacío. |
| 2.2 | Ingresa **Nombre**, selecciona **Servicios** y define **Horario**. |
| 2.3 | `Guardar` → JS valida.<br>Si todo es correcto, inserta un objeto en `localStorage.salas[]` y refresca la tabla (animación “fila nueva”). |

### 3. Editar  
| Paso | Descripción |
|------|-------------|
| 3.1 | `click` **Editar** en la fila deseada. Modal con datos precargados. |
| 3.2 | Modifica campos → `Guardar`. |
| 3.3 | Objeto correspondiente se sobrescribe en `localStorage` y la fila se actualiza al cerrar el modal. |

### 4. Bloquear / Liberar horario (opcional)  
| Paso | Descripción |
|------|-------------|
| 4.1 | Dentro del modal de edición, `click` **«Bloquear horario»**. |
| 4.2 | Selecciona rango y motivo → se agrega un objeto a `localStorage.bloqueos[]`. |
| 4.3 | La vista Agenda pinta el tramo bloqueado en rojo; el slot queda inhabilitado para pruebas de reprogramación. |
| 4.4 | Para liberar, misma ruta → `Eliminar bloqueo`. |

### 5. Eliminar (borrado visual)  
| Paso | Descripción |
|------|-------------|
| 5.1 | `click` **Eliminar** en la fila. Aparece confirmación (`alert`). |
| 5.2 | Si acepta, la fila se quita de la tabla y del arreglo. *(No se revisan citas futuras—limitación del prototipo).* |

---

## **Excepciones (validaciones en front-end)**  

| Código | Caso | Mensaje (ejemplo) |
|--------|------|-------------------|
| EX-01  | **Nombre duplicado** | “Ya existe una sala con ese nombre.” |
| EX-02  | **Nombre inválido** (caracteres especiales) | “Nombre inválido; use solo letras y números.” |
| EX-03  | **Servicios vacíos** | “Seleccione al menos un servicio.” |
| EX-04  | **Horario fuera de rango** o Fin ≤ Inicio | “Horario inválido (09 h – 18 h y fin > inicio).” |

> Todos los mensajes se muestran mediante `alert`, `toast` o `snackbar` en la misma página.

---

## **Resultados Esperados (mundo prototipo)**  

| Acción | Efecto inmediato | Persistencia |
|--------|------------------|--------------|
| **Crear** | Nueva fila aparece en la tabla con animación. | Se agrega al `localStorage`. |
| **Editar** | Datos actualizados en la fila. | Objeto sobrescrito en `localStorage`. |
| **Eliminar** | Fila desaparece. | Objeto removido de `localStorage`. |
| **Bloquear** | Slots pintados en rojo en Agenda. | Registro en `localStorage.bloqueos[]`. |

---

## **Notas Adicionales**  

1. **Monousuario**: cada navegador es una instancia aislada; no hay WebSocket ni sincronía.  
2. **Bitácora ficticia**: los “logs” se imprimen en consola.  
3. **Integridad referencial**: el prototipo **no** impide borrar salas usadas en citas porque las citas también son objetos locales.  
4. **Migración futura**: al pasar a backend se reemplazarán accesos a `localStorage` por API REST/GraphQL y se activarán reglas de negocio reales (ej. no eliminar sala con citas activas).  
5. **Pruebas Rápidas**: para restablecer el estado basta con “Limpiar datos de sitio” o abrir en incógnito.

---

