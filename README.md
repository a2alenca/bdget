EFT - Desarrollo Cloud Native 
Este repositorio tiene el código de la Evaluación Final Transversal. 
El sistema funciona con microservicios en Java, usa colas para procesar las inscripciones pesadas, guarda archivos en la nube, se autentica con Azure y maneja las rutas con un API Manager.

Tecnologías que usamos

*   Backend: Java 17 con Spring Boot y securizado con Spring Security.
*   BFF (Backend for Frontend): El microservicio que orquesta todo y manda los mensajes a la cola.
*   Mensajería: RabbitMQ corriendo en un contenedor Docker. Los productores y consumidores están programados en Java.
*   Base de Datos: Oracle Database (los scripts están metidos en la carpeta `/database`).
*   Autenticación (IDaaS): Configuramos una app en Azure para controlar el inicio de sesión y los usuarios.
*   API Manager: Para registrar y controlar todos los endpoints del backend.
*   CI/CD: Pipeline con GitHub Actions para desplegar automáticamente a la nube de AWS.

