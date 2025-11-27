# Actividad-4-Utilizando-sistemas-de-control-de-versiones

# Casos de uso 


# CU01 – Inicio y Cierre de Sesión

## 🧑 Actor
Usuario registrado

## 📝 Descripción
El usuario ingresa su correo y contraseña.  
Si las credenciales coinciden con las almacenadas en `localStorage`, se inicia una sesión y se redirige al dashboard.  
El cierre de sesión limpia los datos almacenados de sesión y devuelve al usuario a la página de login.

## ⚙️ Precondición
El usuario debe estar registrado en el sistema.

## 📌 Postcondición
Se genera o elimina una sesión activa.

## 🔄 Flujo Principal
1. El usuario accede a `login.html`.
2. Ingresa email y contraseña.
3. Se validan los datos usando `localStorage`.
4. Si son válidos → redirección a `dashboard.html`.
5. Para cerrar sesión, el usuario presiona "Cerrar sesión" → se elimina la sesión.

## 🧪 Criterios de Aceptación
- No avanzar al dashboard si los datos son incorrectos.
- Mantener la sesión mientras el usuario no cierre sesión.
- Mensaje de error si las credenciales son inválidas.



# CU02 – Creación de Tarjetas de Tareas

## 🧑 Actor
Usuario autenticado

## 📝 Descripción
El usuario puede crear una tarjeta ingresando **título, descripción, fecha límite y estado** (por hacer, en progreso, completada).  
Los datos se almacenan en `localStorage` y se muestran visualmente en el dashboard.

## ⚙️ Precondición
El usuario debe haber iniciado sesión.

## 📌 Postcondición
Se crea una tarjeta visible en la interfaz.

## 🔄 Flujo Principal
1. Usuario hace clic en “Nueva tarea”.
2. Se abre un formulario de creación.
3. Ingresa los datos requeridos.
4. La tarjeta se guarda y se muestra en el dashboard.

## 🧪 Criterios de Aceptación
- Ningún campo obligatorio debe quedar vacío.
- La tarjeta debe aparecer inmediatamente después de crearse.
- Los datos deben persistir en `localStorage`.


# CU03 – Edición de Tareas

## 🧑 Actor
Usuario autenticado

## 📝 Descripción
El usuario puede modificar una tarjeta existente: título, descripción, fecha o estado.  
Los cambios se guardan en `localStorage` y se actualizan visualmente.

## ⚙️ Precondición
La tarea debe existir.

## 📌 Postcondición
La tarjeta se actualiza y se refleja en pantalla.

## 🔄 Flujo Principal
1. Usuario selecciona una tarjeta.
2. Hace clic en “Editar”.
3. Modifica los datos.
4. Guarda y se actualiza la tarjeta.

## 🧪 Criterios de Aceptación
- Los cambios deben quedar guardados.
- La vista debe actualizarse automáticamente.
- No se puede dejar una tarjeta sin título.

