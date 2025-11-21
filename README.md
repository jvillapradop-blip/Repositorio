# Resumen del Sistema de Registro de Usuarios

## Descripcion del caso 

El Sistema de Registro de Usuarios tiene como objetivo ofrecer una forma segura y eficiente para que los usuarios accedan a nuestra plataforma. Este sistema se encarga de gestionar la identidad digital de cada usuario, desde el momento en que se registran por primera vez hasta su autenticación y el manejo de su perfil dentro del sistema. Su propósito es garantizar que solo usuarios autorizados puedan acceder a sus cuentas y que puedan gestionar su información de manera sencilla y segura.



## Objetivo del sistema 
El objetivo principal del Sistema de Registro de Usuarios es proporcionar un acceso seguro y confiable a la plataforma.

Su propósito se centra en:

* Gestionar la identidad digital de cada usuario, desde el registro inicial hasta la autenticación y la administración de su perfil.
* Imponer políticas de contraseñas robustas para garantizar la seguridad de las cuentas de usuario y proteger la información personal.


## REQUERIMIENTOS

### Requerimientos Funcionales (RF)
* RF1 - Bloquear temporalmente la cuenta tras 5 intentos fallidos de inicio de sesión.

* RF2 - Mostrar la fecha, hora e IP del último acceso para seguridad.

* RF3 - Rechazar el registro si se usa un correo electrónico temporal.

* RF4 - Permitir al usuario la desactivación reversible de su cuenta (datos retenidos 90 días).

* RF5 - Ofrecer formularios de registro e inicio de sesión en al menos español e inglés.


### Requerimientos Funcionales (RNF)
* RNF1 - Seguridad: Almacenamiento de tokens solo en cookies seguras.

* RNF2 - Compatibilidad: Interfaz responsiva en los principales navegadores.

* RNF3 - Usabilidad: Mensajes de error específicos junto al campo de formulario afectado.


# Casos de prueba (sin tabla)



---

**CP1**

* **Tipo:** Unitario
* **Requerimiento asociado:** Registro de nuevo usuario (datos válidos).
* **Datos:** Nombre: Ana Pérez, Correo: anaperez@email.com, Contraseña: P@sswOrd123.
* **Resultado esperado:** Registro exitoso y usuario guardado.
* **Resultado obtenido:** Éxito.

---

**CP2**

* **Tipo:** Unitario
* **Requerimiento asociado:** Correo electrónico único.
* **Datos:** Intento de registro con correo ya existente (anaperez@email.com).
* **Resultado esperado:** Rechazo y error por duplicidad.
* **Resultado obtenido:** Error: El correo electrónico ya está registrado.

---

**CP3**

* **Tipo:** Unitario
* **Requerimiento asociado:** Longitud mínima de contraseña (8 caracteres).
* **Datos:** Contraseña demasiado corta (corto123 - 7 caracteres).
* **Resultado esperado:** Rechazo y error por longitud mínima.
* **Resultado obtenido:** Error: La contraseña debe tener al menos 8 caracteres.

---

**CP4**

* **Tipo:** Validación
* **Requerimiento asociado:** Campos obligatorios (Nombre).
* **Datos:** Intento de registro con el campo Nombre vacío.
* **Resultado esperado:** Error de validación: El campo Nombre es obligatorio.
* **Resultado obtenido:** Éxito (Error de Validación mostrado).

---

**CP5**

* **Tipo:** Validación
* **Requerimiento asociado:** Formato de correo válido.
* **Datos:** Correo inválido (correoinvalido.com - sin '@').
* **Resultado esperado:** Error de validación: Formato de correo incorrecto.
* **Resultado obtenido:** Éxito (Error de Validación mostrado).


## Tipo de Mantenimiento Propuesto

* Correctivo: Este mantenimiento se enfoca en solucionar problemas que afectan el funcionamiento del sistema.
Ejemplo: Reparar fallos en el inicio de sesión o corregir errores de visualización
* Adaptativo: Su objetivo es hacer ajustes al sistema para que siga funcionando correctamente en entornos cambiantes, como actualizaciones de software o cambios en el hardware.
Ejemplo: Adaptar el sistema a nuevas versiones de un sistema operativo o integrar nuevas tecnologías.
* Perfectivo: Busca mejorar el rendimiento del sistema o añadir nuevas funciones que incrementen su valor para los usuarios.
Ejemplo: Mejorar la velocidad de carga de la aplicación o agregar nuevas características, como opciones de personalización del perfil.
* Preventivo: Se realiza para evitar problemas futuros y asegurar que el sistema siga siendo fácil de mantener con el tiempo.
Ejemplo: Limpiar el código redundante o actualizar dependencias para evitar vulnerabilidades.


## Reflexión sobre el Control de Versiones
El control de versiones juega un papel clave en la gestión de sistemas que manejan información crítica, como los sistemas de autenticación y seguridad de usuarios. Asegura que todas las modificaciones en el código sean rastreables y permite tener un historial claro de los cambios, lo cual es fundamental para mantener la seguridad, la coherencia y la transparencia en el desarrollo.
Además, el control de versiones facilita la validación continua del sistema. Al registrar cada cambio, podemos verificar fácilmente si el sistema sigue cumpliendo con los requisitos de seguridad, como el cifrado de contraseñas, y con los estándares de rendimiento. Esta trazabilidad no solo ayuda a prevenir problemas, sino que también permite auditar y garantizar que las nuevas funcionalidades se implementen de acuerdo con las especificaciones originales.
