# Historia de Usuario 1: Registrar la Compra de Acciones

**Como** usuario,  
**quiero** registrar la compra de acciones,  
**para** poder llevar un registro de las transacciones realizadas y conocer el valor de las acciones adquiridas.

## Criterios de Aceptación

### Escenario 1: Ingresar el Símbolo Bursátil
- **Dado que** el usuario esta en el formulario para registrar la compra de acciones,  
- **Cuando** ingresa un símbolo bursátil válido (como "AAPL" o "TSLA"),  
- **Entonces** el sistema debe aceptar el simbolo ingresado.

### Escenario 2: Ingresar la Fecha de Compra
- **Dado que** el usuario esta en el formulario para registrar la compra de acciones,  
- **Cuando** selecciona en un calendario una fecha válida de compra,  
- **Entonces** el sistema debe aceptar y mostrar la fecha correctamente.

### Escenario 3: Ingresar la Cantidad de Acciones Compradas
- **Dado que** el usuario esta en el formulario de compra de acciones,  
- **Cuando** ingresa una cantidad válida de acciones (número positivo entero),  
- **Entonces** el sistema debe aceptar y mostrar la cantidad de acciones correctamente.

### Escenario 4: Ingresar el Valor de Compra de Cada Acción
- **Dado que** el usuario esta en el formulario de compra de acciones,  
- **Cuando** ingresa un valor de compra válido para cada acción (número positivo con decimales),  
- **Entonces** el sistema debe aceptar y mostrar el valor de compra de las acciones correctamente.

### Escenario 5: Almacenar los Datos de Forma Segura en la Base de Datos
- **Dado que** los datos de la compra de acciones son ingresados correctamente,  
- **Cuando** se haga clic en el botón de registrar,  
- **Entonces** los datos deben ser almacenados correctamente en la base de datos de manera segura.

### Escenario 6: Confirmación de Registro Exitoso
- **Dado que** los datos de la compra de acciones han sido registrados correctamente,  
- **Cuando** el registro se complete exitosamente,  
- **Entonces** el sistema debe mostrar un mensaje de confirmación indicando que la compra ha sido registrada con éxito.

### Escenario 7: Ingresar un Símbolo Bursátil Inválido
- **Dado que** el usuario esta en el formulario para registrar la compra de acciones,  
- **Cuando** ingresa un símbolo bursátil que no existe,  
- **Entonces** el sistema debe mostrar un mensaje de error indicando que el símbolo ingresado no existe.  

### Escenario 8: Ingresar una Cantidad Negativa de Acciones
- **Dado que** el usuario esta en el formulario para registrar la compra de acciones,  
- **Cuando** ingresa una cantidad negativa de acciones,  
- **Entonces** el sistema debe mostrar un mensaje de error de invalidez de números negativos  

### Escenario 9: Ingresar un Valor de Compra Negativo
- **Dado que** el usuario esta en el formulario para registrar la compra de acciones,  
- **Cuando** ingresa un valor de compra negativo para una acción,  
- **Entonces** el sistema debe mostrar un mensaje de error de invalidez de números negativos
## Tareas

1. Crear un formulario para ingresar el simbolo Bursatil, la fecha, cantidad de acciones y valor de compra.
2. Configurar la base de datos para registrar la información de la compra.
3. Crear un método en el backend que registre los datos de la compra de acciones.
4. Implementar una notificación de éxito cuando los datos se hayan registrado correctamente.
5. Validar el campo del símbolo bursátil en el formulario para que acepte únicamente simbolos existentes
6. Validar el campo de Valor de compra y Cantidad de acciones en el formulario para que acepte únicamente.

# Historia de Usuario 2: Ver Detalles de un Registro

**Como** usuario,  
**quiero** poder seleccionar un registro específico de mis compras de acciones,  
**para** ver los detalles  del registro seleccionado.

## Criterios de Aceptación

### **Escenario 1: Ver Detalles de un Registro**
**Dado** que el usuario observa la lista de registros de compra de acciones,  
**Cuando** el usuario selecciona un registro específico,  
**Entonces** el sistema debe mostrar los detalles de ese registro.

## Tareas
1. Actualizar la interfaz del usuario para mostrar todos los registros de compra de acciones.
2. Implementar la funcionalidad para que el usuario pueda seleccionar un registro específico de la lista.
3. Crear la interfaz para mostrar los detalles del registro seleccionado.



# Historia de Usuario 3: Cálculo de Ganancia/Pérdida
**Como** usuario,  
**quiero** ver la ganancia o pérdida de mis acciones,  
**para** poder evaluar el rendimiento de mi inversión en tiempo real.

## Criterios de Aceptación

### **Escenario 1: Ver Ganancia**
**Dado** que el usuario ha registrado una compra de acciones con un valor de compra determinado,  
**Cuando** el usuario consulta la ganancia en la fecha actual,  
**Entonces** el sistema debe calcular el porcentaje de ganancia, mostrando un valor positivo si el valor actual de las acciones es mayor que el valor de compra.

---

### **Escenario 2: Ver Pérdida**
**Dado** que el usuario ha registrado una compra de acciones con un valor de compra determinado,  
**Cuando** el usuario consulta la pérdida en la fecha actual,  
**Entonces** el sistema debe calcular el porcentaje de pérdida, mostrando un valor negativo si el valor actual de las acciones es menor que el valor de compra.

---

### **Escenario 3: Mostrar el Porcentaje de Ganancia/Pérdida**
**Dado** que el cálculo de ganancia o pérdida ha sido realizado,  
**Cuando** el usuario ve el resultado,  
**Entonces** el sistema debe mostrar el porcentaje de ganancia o pérdida de forma clara, indicando si es un valor positivo (ganancia) o negativo (pérdida).


## Tareas

1. Implementar la lógica para calcular la ganancia cuando el valor actual de las acciones es mayor que el valor de compra.
2. Implementar la lógica para calcular la pérdida cuando el valor actual de las acciones es menor que el valor de compra.
3. Crear una interfaz para mostrar el porcentaje de ganancia o pérdida, la ganancia y la perdida al usuario.


# Historia de Usuario 4: Ordenamiento de Acciones

**Como** usuario,  
**quiero** ordenar por nombre mis acciones de forma ascendente,  
**para** visualizar mis inversiones en orden alfabético y facilitar su búsqueda.

## Criterios de Aceptación

### **Escenario 1: Ordenar Acciones Ascendentemente**
**Dado** que el usuario visualiza la lista de acciones,  
**Cuando** haga clic en el botón de ordenamiento,  
**Entonces** el sistema debe reordenar la lista de acciones de forma ascendente (alfabéticamente por el nombre).


## Tareas

1. Desarrollar la función en el backend que ordene las acciones de forma ascendente.
2. Integrar el botón de ordenamiento en la interfaz de usuario.

---

# Historia de Usuario 5: Consolidación de Acciones

**Como** usuario,  
**quiero** ver un consolidado de mis acciones que incluya el porcentaje de ganancia o pérdida de cada acción,  
**para** evaluar de forma global el rendimiento de mis inversiones.

## Criterios de Aceptación

### **Escenario 1: Mostrar Consolidado de Acciones**
**Dado** que el usuario ha registrado múltiples acciones,  
**Cuando** consulte la sección de consolidado,  
**Entonces** el sistema debe agrupar las acciones similares y mostrar el porcentaje de ganancia o pérdida para cada grupo.

## Tareas

1. Implementar la lógica para agrupar acciones duplicadas y calcular el porcentaje de ganancia o pérdida.
2. Crear un DTO para facilitar el envío de la información consolidada al frontend.
3. Diseñar la interfaz para mostrar el consolidado de acciones de manera clara y ordenada.

---

# Historia de Usuario 6: Inicio de Sesión y Registro con Token Seguro

**Como** usuario,  
**quiero** iniciar sesión y registrarme de forma segura,  
**para** mantener mi sesión activa en la página  sin tener que reingresar mis credenciales continuamente.

## Criterios de Aceptación

### **Escenario 1: Registro y Generación de Token**
**Dado** que un usuario se registra en la plataforma,  
**Cuando** complete el proceso de registro,  
**Entonces** el sistema debe generar un token seguro y enviarlo al cliente para iniciar la sesión.

### **Escenario 2: Inicio de Sesión y Mantenimiento de Sesión**
**Dado** que el usuario inicia sesión correctamente,  
**Cuando** se autentique,  
**Entonces** el sistema debe enviar el token en el encabezado de las solicitudes, manteniendo la sesión activa y segura.

## Tareas

1. Crear la vista de login y registro en el frontend.
2. Implementar la lógica de autenticación en el backend utilizando JWT.
3. Configurar el almacenamiento y validación del token en la aplicación cliente.

---

# Historia de Usuario 7: Paginación para el Registro de Acciones Compradas

**Como** usuario,  
**quiero** visualizar mis acciones compradas en páginas,  
**para** navegar de manera eficiente a través de un gran volumen de registros.

## Criterios de Aceptación

### **Escenario 1: Visualización de la Paginación**
**Dado** que el usuario tiene numerosas acciones compradas,  
**Cuando** revise los registros de las acciones compradas,  
**Entonces** el sistema debe mostrar un menú de páginas, limitando la cantidad de registros mostrados por página.

### **Escenario 2: Navegación Entre Páginas**
**Dado** que existen múltiples páginas de registros,  
**Cuando** el usuario seleccione una página específica,  
**Entonces** los registros de acciones deben actualizarse para mostrar únicamente los registros correspondientes a esa página.

## Tareas
1. Implementar la lógica de paginación en el backend, limitando el número de registros por página.
2. Diseñar e integrar el menú de páginas en la interfaz de usuario.
