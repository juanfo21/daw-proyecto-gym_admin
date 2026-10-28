Anteproyecto: Gym-Admin



Módulo: Proyecto Intermodular (0379 · PIDW2) — 2º DAW Virtual



Centro: CIFP Avilés (Curso 2026/2027)



Autor/a: Juan Fernández Ordiales



Repositorio GitHub: https://github.com/juanfo21/daw-proyecto-gym\_admin



Tablero GitHub Projects: https://github.com/users/juanfo21/projects/2



\---



\## 1. Justificación y dominio funcional



\### 1.1. Elevator pitch (100–150 palabras)



Este proyecto consiste en la creación de un programa para un gimnasio que servirá para gestionar turnos en las maquinas y equipos de el propio gimnasio

para así facilitar el orden durante los entrenamientos mediante el uso de un Sistema de usuarios registrados los socios podrán reservar equipamiento

y tener prioridad a la hora de usar el mismo durante un tiempo prestablecido, esto Tambien permitirá la gestion de pagos atreves de el mismo Sistema

y la reserve de sesiones con entrenadores privados e inscribirse en actividades de clubes deportivos registrados en el mismo polideportivo.

De este modo el programa reunirá todas estas funciones en un espacio digital.





\### 1.2. Público objetivo y contexto de uso



El publico objetivo serian los gestores de el gimnasio, los entrenador privados, los socios de el gimnasio y los clubes deportivos.



Posibles usos serian:



* Gestionar los dispositivos de el gimnasio en hora punta.
* Centralizar la gestion de los diferentes clubes en un solo lugar.
* Planificar los entrenamientos con entrenadores personales.
* Manejar el pago y renovación de membresía online para eliminar la necesidad de pasar por recepción.





\## 2. Roles del sistema y casos de uso



\### 2.1. Matriz de roles (RBAC) -



Administrador: Gestion de cuentas, roles, maquinas y sus franjas de disponibilidad, sesiones con entrenadores y registros en los clubes.



Usuario registrado: Consultar la disponibilidad y registrar turno en el equipamiento, realizar pagos, registrarse en clubes y gestionar su propio perfil.



Público / invitado: Pude consultar información publica de el gimnasio y registrarse en la pagina.

&#x20;

\### 2.2. Casos de uso principales (mínimo 6)



1\. CU-01: Registro e inicio de sesión seguro con tokens JWT.



2\. CU-02: Gestionar equipos y franjas disponibles.



3\. CU-03: Gestionar la oferta de sesiones con entrenadores.



4\. CU-04: Reservar y cancelar turnos en los equipos.



5\. CU-05: Realizar pagos de la membresía.



6\. CU-06: Registrarse como miembro de los diferentes clubes.



7\. CU-07: Consultar información sobre el gimnasio y los diferentes clubes.



8\. CU-08: Gestionar cambios en el perfil de usuario.



\### 2.3. Alcance del MVP (Hito 3, diciembre) -



Incluido: \[Casos de uso operativos en producción en diciembre.] -



&#x09;CU-01: Registro e inicio de sesión seguro con tokens JWT.



&#x09;CU-02: Gestionar equipos y franjas disponibles.



&#x09;CU-03: Gestionar la oferta de sesiones con entrenadores.



&#x09;CU-04: Reservar y cancelar turnos en los equipos.



&#x09;CU-08: Gestionar cambios en el perfil de usuario.





Fuera del MVP: \[Funcionalidades que se abordarán con los Add-ons o quedan como líneas futuras.] ---



&#x09;CU-05: Realizar pagos de la membresía.

&#x09;

&#x09;CU-06: Registrarse como miembro de los diferentes clubes.



&#x09;CU-07: Consultar información sobre el gimnasio y los diferentes clubes.



\## 3. Modelo de datos -



&#x20;Diagrama Entidad-Relación en 3FN:



&#x20;	Relación 1:N: \[SOCIO → RESERVA\_MAQUINA]

&#x09;

&#x09;Relación 1:N: \[MAQUINA A → RESERVA\_MAQUINA]



&#x09;Relación 1:N: \[SOCIO → PAGO]



&#x09;Relación 1:N: \[SOCIO → SESION\_ENTRENAMIENTO]



&#x09;Relación 1:N: \[ENTRENADOR → SESION\_ENTRENAMIENTO]



&#x20;	Relación M:N:\*\* \[SOCIO ↔ CLUB mediante REGISTRO\_CLUB(id\_socio, id\_club)]



\## 4. Stack tecnológico previsto -



Motor de base de datos: MySQL



es una tecnología ampliamente utilizada, con abundantes recursos de aprendizaje.



Backend API: Node.js



su arquitectura basada en operaciones asíncronas resulta adecuada para gestionar las solicitudes de los usuarios, las consultas a la base de datos y las operaciones de reserva.



Frontend: Next.js



Integración con Node.js, comparte el ecosistema JavaScript facilita añadir nuevas páginas

y funcionalidades sin tener que construir toda la estructura de la aplicación desde cero.





Alojamiento cloud previsto: Railway



integración directa con MySQL, configuración centralizada y despliegue sencillo de frontend y backend



\## 5. Selección tentativa de Add-ons



\- Pasarela de pagos Stripe en entorno Sandbox con Webhooks



\- WebSockets / Comunicación en tiempo real



