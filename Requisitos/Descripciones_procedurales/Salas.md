# **Nombre del Proceso:**  
## Administración de consultorios

---

## **Objetivo**  
_Crear y actualizar la información de los consultorios, como el nombre y el tipo._

---

## **Actores**  
- **Coordinadora:** Ejecuta la creación o edición de datos del consultorio.

---

## **Entradas**  
- Nombre del consultorio.  
- Tipo de consultorio, basado en el tipo de contacto o la edad del paciente.

---

## **Pasos**  

### En caso de eliminación  
1. **Verificación:** La Coordinadora ingresa a la sección de consultorios de la barra de navegación y verifica en el listado de consultorios que este ha sido creado.  
2. **Eliminación:** Una vez verificado, presiona el botón “Eliminar” en la fila del consultorio en la lista, lo que abrirá un mensaje de confirmación.  
3. **Confirmación:** La Coordinadora confirma la eliminación del consultorio y el sistema le notifica que el consultorio fue eliminado con éxito.  
4. **Registro de cambios:** El sistema registra los cambios y actualiza el listado de consultorios.  

### En caso de creación  
1. **Verificación:** La Coordinadora ingresa a la sección de consultorios de la barra de navegación y verifica en el listado de consultorios que este aún no esté creado.  
2. **Apertura de formulario:** Una vez verificado, presiona el botón “Agregar Nuevo Consultorio”, lo que abrirá un formulario.  

### En caso de edición  
1. **Verificación:** La Coordinadora ingresa a la sección de consultorios de la barra de navegación y verifica que el consultorio esté en la lista.  
2. **Apertura de formulario:** Una vez verificado, presiona el botón “Editar”, lo que abrirá un formulario.  

### Para creación y edición  
3. **Ingreso de nombre y tipo:** La Coordinadora introduce el nombre asignado y el tipo del consultorio, basado en si es de primer contacto o a las personas que atiende (niños o adultos), posteriormente guarda esos cambios.  
4. **Solicitud de confirmación:** El sistema solicita una confirmación para llevar a cabo la creación del consultorio.  
5. **Confirmación:** La Coordinadora confirma la creación/edición del consultorio y el sistema le notifica que el consultorio fue creado/editado con éxito.  
6. **Registro del consultorio y cierre:** El sistema registra los cambios y actualiza el listado de consultorios.

---

## **Excepciones**  
- **Nombre repetido:**  
  En caso de que se ingrese un nombre ya registrado en el sistema con otro consultorio, se notificará que el nombre ya está en uso y no se llevará a cabo la creación/edición del consultorio hasta que se ingrese un nombre no repetido.  

- **Nombre inválido:**  
  En caso de que el nombre contenga caracteres inválidos como caracteres especiales y signos de puntuación, se notificará que el nombre contiene caracteres inválidos y no se llevará a cabo la creación/edición del consultorio hasta que se ingrese un nombre válido.

---

## **Resultados Esperados**  
- En caso de crear un nuevo consultorio, este deberá registrarse en el sistema y aparecer en una nueva fila del listado de consultorios.  
- En caso de editar un consultorio, los datos editados deberán registrarse y aparecer en la lista (en la fila del consultorio editado).  
- En caso de eliminar un consultorio, el consultorio deberá eliminarse del sistema y dejar de visualizarse en la lista.

---

## **Notas Adicionales**  
- Este proceso corresponde a la Coordinadora, al ser un proceso que puede comprometer la gestión de citas de la clínica.  
- Es importante que la eliminación o edición de un consultorio no afecte directamente a citas ya programadas. En caso de que sí lo haga, se deberá notificar y coordinar la reprogramación de las citas afectadas si es necesario.

---
