## INTRODUCIÓN AL SISTEMA

El *New Reset A.H.I.D.* es sistema prototipo de gestión de incidencias para equipos. Donde se registren, solucionen y midan los tiempos de atención en las incidencias.

### Características y funcionalidades principales

El código fuente se encuentra disponible para bajar desde el portal del *GitHub* a través de la dirección [https://github.com/andgar2010/Project_New_Reset_AIHD](https://github.com/andgar2010/Project_New_Reset_AIHD.) Su implementación fue realizada en *Apache* y *PHP7* o superior y el sistema de manejo de bases de datos en *MySQL* o *MariaDB*.

El sistema tiene varias funcionalidades y entre ellas se destacan:

* Registro nueva cuenta de usuarios para ingresar el sistema y login a los usuarios;
* Añadir, modificar y eliminar un equipo;
* Crear, modificar y eliminar un usuario;
* Crear, modificar y eliminar una incidencia;
* Informes de las incidencias y notificaciones después de su nueva incidencia al encargado;

* Soporte a idioma: Español.

### Arquitectura

#### Requisitos generales para la instalación

* Un servidor con el sistema operativo *GNU/Linux* preferido o servicio de hosting de sitio *Linux* con suporte a *PHP* y base de datos *MySQL*.

* Disponibilidad de almacenamiento mínimo de 10 Gigabytes para guarda de archivos e instalación del sistema.

* Se recomienda un sistema de respaldo \(backup\) por *FTP* o *backup automático* en el caso de servidor dedicado.

* Conexión con la Internet en banda ancha, especialmente para los gestores del sistema.

* Tener instalado el cliente *GIT* el caso que se optó por instalar el sistema a través del servicio *GitHub*.

#### Requisitos previos

Acerca de servicios y autorizaciones necesarias al sistema se destacan:

* Servicio de correo habilitado en el servidor, permitindo el envio de correo electrónico a través de una dirección de correo autenticada.

* Tener el directorio “repositorio” con permisos de escritura y lectura para transferir y almacenar archivos.

* Se recomenda habilitar el *CURL* para acceso de actualizaciones del sistema \(opcional\)

NOTA: Garantizar que el *short\_open\_tag* está configurada como *On* en el archivo php.ini. De otra manera, el proceso de logon fallará.



© 2018 New Reset A.I.H.D., Inc.

