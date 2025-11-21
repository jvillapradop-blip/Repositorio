# ***Mantenimiento Propuesto para el Sistema de Registro de usuario***

## ***1. Problema: Dificultades en el proceso de validación de correo electrónico***



El sistema no verifica correctamente la validez del correo electrónico durante el proceso de registro, lo que permite que los usuarios ingresen direcciones de correo no válidas o mal formateadas, afectando la comunicación y la seguridad del sistema.


  ***Tipo de Mantenimiento:*** Mantenimiento correctivo

  

  ***Acción Principal:*** Revisar y corregir el proceso de validación de direcciones de correo electrónico en el sistema. Implementar un algoritmo de validación más robusto que asegure que las direcciones de correo ingresadas sean correctas y estén bien formateadas antes de permitir el registro.


  ***Justificación Técnica:*** Este problema no es un error grave, pero puede ocasionar inconvenientes al momento de contactar a los usuarios o para la recuperación de contraseñas. Mejorar la validación del correo electrónico garantiza que solo se registren direcciones válidas, lo que mejora la calidad de los datos almacenados y reduce problemas futuros relacionados con la comunicación, además de optimizar la integridad del sistema de autenticación.


## ***2. Problema: Incompatibilidad con navegadores antiguos***



  El sistema presenta problemas de funcionamiento en versiones antiguas de navegadores web, lo que impide que algunos usuarios completen el proceso de registro o accedan a sus cuentas correctamente.



  ***Tipo de Mantenimiento:*** Mantenimiento adaptativo



  ***Acción Principal:*** Actualizar y optimizar el código frontend para garantizar la compatibilidad con versiones anteriores de navegadores web. Esto incluye el uso de tecnologías web estándar y la implementación de polyfills o soluciones alternativas para funciones que no son soportadas en versiones más antiguas de navegadores.


  ***Justificación Técnica:*** Este problema no es un error del sistema, sino que surge por la evolución de los navegadores web. Adaptar el sistema para ser compatible con versiones anteriores garantizará que los usuarios con navegadores más antiguos puedan registrarse y acceder al sistema sin inconvenientes, aumentando la accesibilidad y mejorando la experiencia del usuario. Además, evitará que se pierdan potenciales usuarios debido a incompatibilidades tecnológicas.


