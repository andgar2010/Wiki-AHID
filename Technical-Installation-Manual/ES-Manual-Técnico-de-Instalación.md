![](https://github.com/andgar2010/Project_New_Reset_AIHD/raw/master/WEB/assets/images/LogoV2.png)

# MANUAL TÉCNICO DE INSTALACIÓN
* Proyecto: NEW RESET A.I.H.D.
* Versión 0.0.1


| DESCRIPCIÓN | MANUAL DE INSTALACIÓN Y CONFIGURACIÓN NEW RESET A.I.H.D. |
| ----------- | ---------------------------------------- |
|             |                                          |


| ACTUALIZACIÓN | IDIOMA  | REVISIÓN |
| ------------- | ------- | -------- |
| 23/ene./2015  | ESPAÑOL | 0.0.1    |
|               |         |          |


###CONTROL DE REVISIONES

| FECHA        | RESPONSABLE                  | ACCIÓN                 |
| ------------ | ---------------------------- | ---------------------- |
| 07/mar./2018 | Andrés Felipe García Ramírez | Creación del Documento |
| 7/mar./2018  | BIREME/MTI/RST/acs           | Revisión del Documento |
|              |                              |                        |




## LICENCIA DEL SISTEMA

*New Reset A.H.I.D.* es una colaboración entre la *Organización* y la *Universidad*. Todos los derechos son reservados a la *Organizacion*.

## INTRODUCIÓN AL SISTEMA

El *New Reset A.H.I.D.* es un sistema de gestión de evaluación de las comisiones de ética en investigación, proponiendo una metodología de sometimiento, evaluación y manejo de los protocolos sometidos para apreciación de las comisiones de ética. 

### Características y funcionalidades principales 

El código fuente se encuentra disponible para bajar desde el protal del *GitHub* a través de la dirección https://github.com/andgar2010/Project_New_Reset_AIHD. Su implementación fue realizada en *Apache*&trade; y *PHP7* o superior y el sistema de manejo de bases de datos en *MySQL*&trade;. 

El sistema tiene varias funcionalidades y entre ellas se destacan: 
* Sometimiento de protocolos de investigación para evaluación ética; 
* Almacenamiento de documentos; 
* Sometimiento de correciones, informes de eventos adversos y notificaciones después de su aprobación; 
* Suporte a múltiples idiomas, sendo nativos el Portugués de Brasil, Español, Inglés y Francés; 
* Evaluación por un o múltiples relatores; 
* Acceso a los protocolos por todos los miembros de la comisión; 
* Interoperabilidad de datos con los 20 campos de la OMS para ensayos clínicos (habilitación opcional); 
* Comunicación con investigadores a través de correo electrónico y  registro de las comunicaciones. 

### Arquitectura 

#### Requisitos generales para la instalación 

* Un servidor con el sistema operativo *GNU/Linux* preferido o servicio de hosting de sitio *Linux* con suporte a *PHP*&trade; y base de datos *MySQL*&trade;. 
* Disponibilidad de almacenamiento mínimo de 20 Gigabytes para guarda de archivos e instalación del sistema. 
* Se recomienda un sistema de respaldo (backup) por *FTP* o *backup automático* en el caso de servidor dedicado. 
* Conexión con la Internet en banda ancha, especialmente para los gestores del sistema. 
* Tener instalado el cliente *GIT* el caso que se optó por instalar el sistema a través del servicio *GitHub*. 

#### Requisitos previos  

Acerca de servicios y autorizaciones necesarias al sistema se destacan: 
* Servicio de correo habilitado en el servidor, permitindo el envio de correo electrónico a través de una dirección de correo autenticada. 
* Tener el directorio “repositorio” con permisos de escritura y lectura para transferir y almacenar archivos. 
* Se recomenda habilitar el *CURL* para acceso de actualizaciones del sistema (opcional) 

NOTA: Garantizar que el *short_open_tag* está configurada como *On* en el archivo php.ini. De otra manera, el proceso de logon fallará. 


## INSTALACIÓN  

### Download del sistema  

Hay dos modos para se instalar el sistema: 
* con versionamiento (git); 
* sin versionamento (zip). 

#### Instalación a través de cliente *GIT* (versionamiento)  

Ese es el modo preferible para se instalar el sistema, porque se permite actualizar el aplicativo en modo simple y seguro, y también manteniendo las personalizaciones privadas, configuraciones generales del sistema etc. 

Para instalar el sistema por el cliente del *GIT*, escriba en la linea de comandos de *Linux* - bajo el directorio donde se desea instalar el paquete - el comando abajo: 

 git clone git://github.com/bireme/proethos.git proethos 

#### Instalación por paquete zip  

Para descargar la última versión del sistema New Reset A.H.I.D. acceda el enlace
	https://github.com/andgar2010/Project_New_Reset_AIHD
y haga un clic en el icono “Download ZIP” que se encuentra al lado derecho de la página. 

![](https://raw.githubusercontent.com/bireme/proethos/master/_documents/images/es/image007.png) 

Figura 1 - Icone para *Download* 

Después del clic el sitio de GitHub proporcionará el paquete de la última versión para ser guardado en su computadora. 

![](https://raw.githubusercontent.com/bireme/proethos/master/_documents/images/es/image008.png) 

Figura 2 - Download del *New Reset A.H.I.D.* en formato *ZIP* 

Todo el contenido del archivo deberá ser despaquetado - se recomienda utilizar el aplicativo *WinRar* - y después transportar al servidor web que alojará el sistema. 

![](https://raw.githubusercontent.com/bireme/proethos/master/_documents/images/es/image010.png) 

Figura 3 - Estructura de archivos 

Se recomienda el envio de los archivos por *FTP* o utilizar la instalación del sistema en directo a través del software del *GitHub* para servidores *Linux*.  

### Crear una base de datos en el servidor *MySQL*  

Crea una base de datos en el servidor *MySQL* con el nombre de *'proethos*' - o el nombre que mejor se adapta al servidor instalado o a los criterios de seguridad de la institución. Los datos de ejemplo en seguida serán necesarios para la conexión: 

| Requisito      | Valor(ejemplo)  |
| -------------- | --------------- |
| Servidor       | localhost       |
| Base de datos  | xxNameDBxx      |
| Usuario        | sa_xxNameUserxx |
| Contraseña     | **********      |
| Servidor de BD | MySQL           |


Este archivo solamente será creado una vez. Cualquier cambio en los parámetros del sistema, el archivo de configuración deberá ser borrado del sistema por el administrador técnico a través del *FTP*. 

El archivo de configuración es creado en el directorio *_db* bajo el directorio raíz del sistema. 

### Activación de la conexión con la base de datos 

En el primero acceso del sistema es necesario tener las configuraciones del archivo de conexión con la base de datos. Para que eso pueda occurir, se accede el sistema en su página de instalación a través de cualquier navegador de internet, ej: 
	htttp://localhost:8080/

Si el archivo *_db/db_paho.php* no es localizado, el sistema redirecciona para el area de configuración, presentando la pantalla de la figura 4. 

![](https://raw.githubusercontent.com/bireme/proethos/master/_documents/images/es/image012.png) 

Figura 4 - Pantalla de configuración do archivo *DB* 

En esa pantalla se debe informar el tipo de base de datos (Base Type), con una de las opciones: 
* *MySQL* para se conectar a la base de datos *MySQL* a través del método mysql_connect(), común en  na mayoría de los servidores. 
* *MySQL(PDO)* para acceder la base de datos MySQL utilizando un driver con interfaz PHP Data Objects (PDO). Esa función es utilizada cuando el servidor informa que el método mysql_connect() es obsoleto. 

En el campo *Database host* se debe informar el *IP* o el nombre del servidor de la base de datos. Se puede utilizar *localhost* cuando la base se encuentra en el mismo servidor. 

Los otros campos se refieren a la conexión con la base de datos, como el nombre de la base (*Database name*), usuario de conexión (*User name*) y la contraseña (*Password*). En caso de error, el sistema informa en una caja de texto abajo los problema encuentrados. Si todo estuvier configurado correctamente, el archivo *db_paho.php* es creado automáticamente, informando el mensaje de éxito. 

### Creación manual del archivo de acceso a la base de datos

Se puede optar por crear el archivo *_db/db_paho.php* manualmente, el caso que no se desea habilitar permisos de escritura para el usuario del *Apache* en esta carpeta. Si es así, se debe crear el archivo con el contenido abajo, personalizado para cada servidor. Se debe guardar ese archivo en el subdirectorio *_db* con el nombre *db_paho.php*.

```php
 db.php

 <?php
 /* Data Base - Config */
 
 $base='mysql';          /* o mysqlPDO */
 $base_host='localhost'; /* Nombre del host */
 $base_name='xx NameDB xx';  /* Nombre de la base */
 $base_user='root';      /* Usuario */
 $base_pass='password';  /* Contraseña */

 $ok = db_connect();
 ?>
```

### Inicializar el sistema

En el primer *login* el sistema se encuentra configurado préviamente con el usuario y contraseña abajo:

| Usuario | Contraseña         |
| ------- | ------------------ |
| admin   | ** xxpasswordxx ** |

Es necesario que al iniciar el sistema tiene que executar en el MENÚ del ADMINISTRADOR las funciones Actualizar sistema y Actualizar campos del sistema

## Configurando

### Configuración de los datos de la Comisión

(*Texto en producción*)

### Actualización del software

El caso que el sistema fuera instalado utilizando el cliente *GIT*, será posible actualizar el software siempre que el repositorio del aplicativo es modificado.

Para realizar la actualización, accede en la linea de comandos el directorio del aplicativo (ej.: New Reset A.I.H.D.) y escriba:

```
 git pull

```

NOTA: El caso que hubo personalización en alguna parte del código del aplicativo, el *GIT* informará que hay una inconsistencia para ejecutar la actualización. En ese caso, consulte la documentación de *GitHub* para restablecer los archivos que no se deben incluir en la actualización.



© 2018 New Reset A.I.H.D., Inc.