## INTRODUCIÓN AL SISTEMA

El _New Reset A.H.I.D._ es un sistema de gestión de evaluación de las comisiones de ética en investigación, proponiendo una metodología de sometimiento, evaluación y manejo de los protocolos sometidos para apreciación de las comisiones de ética.

### Características y funcionalidades principales

El código fuente se encuentra disponible para bajar desde el portal del *GitHub* a través de la dirección [https://github.com/andgar2010/Project_New_Reset_AIHD](https://github.com/andgar2010/Project_New_Reset_AIHD.) Su implementación fue realizada en *Apache* y *PHP7* o superior y el sistema de manejo de bases de datos en\_MySQL_.

El sistema tiene varias funcionalidades y entre ellas se destacan:

* Sometimiento de protocolos de investigación para evaluación ética;
* Almacenamiento de documentos;
* Sometimiento de correciones, informes de eventos adversos y notificaciones después de su aprobación;
* Soporte a idioma: Español.

* Evaluación por un o múltiples relatores;
* Acceso a los protocolos por todos los miembros de la comisión;
* Interoperabilidad de datos con los 20 campos de la OMS para ensayos clínicos \(habilitación opcional\);
* Comunicación con investigadores a través de correo electrónico y registro de las comunicaciones.

### Arquitectura

#### Requisitos generales para la instalación

* Un servidor con el sistema operativo *GNU/Linux* preferido o servicio de hosting de sitio *Linux* con suporte a *PHP* y base de datos *MySQL*.

* Disponibilidad de almacenamiento mínimo de 20 Gigabytes para guarda de archivos e instalación del sistema.

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

