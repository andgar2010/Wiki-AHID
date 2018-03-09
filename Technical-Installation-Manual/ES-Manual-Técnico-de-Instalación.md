![](https://github.com/andgar2010/Project_New_Reset_AIHD/raw/master/WEB/assets/images/LogoV2.png)

# MANUAL T�CNICO DE INSTALACI�N
* Proyecto: NEW RESET A.I.H.D.
* Versi�n 0.0.1


| DESCRIPCI�N | MANUAL DE INSTALACI�N Y CONFIGURACI�N NEW RESET A.I.H.D. |
| ----------- | ---------------------------------------- |
|             |                                          |


| ACTUALIZACI�N | IDIOMA  | REVISI�N |
| ------------- | ------- | -------- |
| 23/ene./2015  | ESPA�OL | 0.0.1    |
|               |         |          |


###CONTROL DE REVISIONES

| FECHA        | RESPONSABLE                  | ACCI�N                 |
| ------------ | ---------------------------- | ---------------------- |
| 07/mar./2018 | Andr�s Felipe Garc�a Ram�rez | Creaci�n del Documento |
| 7/mar./2018  | BIREME/MTI/RST/acs           | Revisi�n del Documento |
|              |                              |                        |




## LICENCIA DEL SISTEMA

*New Reset A.H.I.D.* es una colaboraci�n entre la *Organizaci�n* y la *Universidad*. Todos los derechos son reservados a la *Organizacion*.

## INTRODUCI�N AL SISTEMA

El *New Reset A.H.I.D.* es un sistema de gesti�n de evaluaci�n de las comisiones de �tica en investigaci�n, proponiendo una metodolog�a de sometimiento, evaluaci�n y manejo de los protocolos sometidos para apreciaci�n de las comisiones de �tica. 

### Caracter�sticas y funcionalidades principales 

El c�digo fuente se encuentra disponible para bajar desde el protal del *GitHub* a trav�s de la direcci�n https://github.com/andgar2010/Project_New_Reset_AIHD. Su implementaci�n fue realizada en *Apache*&trade; y *PHP7* o superior y el sistema de manejo de bases de datos en *MySQL*&trade;. 

El sistema tiene varias funcionalidades y entre ellas se destacan: 
* Sometimiento de protocolos de investigaci�n para evaluaci�n �tica; 
* Almacenamiento de documentos; 
* Sometimiento de correciones, informes de eventos adversos y notificaciones despu�s de su aprobaci�n; 
* Suporte a m�ltiples idiomas, sendo nativos el Portugu�s de Brasil, Espa�ol, Ingl�s y Franc�s; 
* Evaluaci�n por un o m�ltiples relatores; 
* Acceso a los protocolos por todos los miembros de la comisi�n; 
* Interoperabilidad de datos con los 20 campos de la OMS para ensayos cl�nicos (habilitaci�n opcional); 
* Comunicaci�n con investigadores a trav�s de correo electr�nico y  registro de las comunicaciones. 

### Arquitectura 

#### Requisitos generales para la instalaci�n 

* Un servidor con el sistema operativo *GNU/Linux* preferido o servicio de hosting de sitio *Linux* con suporte a *PHP*&trade; y base de datos *MySQL*&trade;. 
* Disponibilidad de almacenamiento m�nimo de 20 Gigabytes para guarda de archivos e instalaci�n del sistema. 
* Se recomienda un sistema de respaldo (backup) por *FTP* o *backup autom�tico* en el caso de servidor dedicado. 
* Conexi�n con la Internet en banda ancha, especialmente para los gestores del sistema. 
* Tener instalado el cliente *GIT* el caso que se opt� por instalar el sistema a trav�s del servicio *GitHub*. 

#### Requisitos previos  

Acerca de servicios y autorizaciones necesarias al sistema se destacan: 
* Servicio de correo habilitado en el servidor, permitindo el envio de correo electr�nico a trav�s de una direcci�n de correo autenticada. 
* Tener el directorio �repositorio� con permisos de escritura y lectura para transferir y almacenar archivos. 
* Se recomenda habilitar el *CURL* para acceso de actualizaciones del sistema (opcional) 

NOTA: Garantizar que el *short_open_tag* est� configurada como *On* en el archivo php.ini. De otra manera, el proceso de logon fallar�. 


## INSTALACI�N  

### Download del sistema  

Hay dos modos para se instalar el sistema: 
* con versionamiento (git); 
* sin versionamento (zip). 

#### Instalaci�n a trav�s de cliente *GIT* (versionamiento)  

Ese es el modo preferible para se instalar el sistema, porque se permite actualizar el aplicativo en modo simple y seguro, y tambi�n manteniendo las personalizaciones privadas, configuraciones generales del sistema etc. 

Para instalar el sistema por el cliente del *GIT*, escriba en la linea de comandos de *Linux* - bajo el directorio donde se desea instalar el paquete - el comando abajo: 

 git clone git://github.com/bireme/proethos.git proethos 

#### Instalaci�n por paquete zip  

Para descargar la �ltima versi�n del sistema New Reset A.H.I.D. acceda el enlace
	https://github.com/andgar2010/Project_New_Reset_AIHD
y haga un clic en el icono �Download ZIP� que se encuentra al lado derecho de la p�gina. 

![](https://raw.githubusercontent.com/bireme/proethos/master/_documents/images/es/image007.png) 

Figura 1 - Icone para *Download* 

Despu�s del clic el sitio de GitHub proporcionar� el paquete de la �ltima versi�n para ser guardado en su computadora. 

![](https://raw.githubusercontent.com/bireme/proethos/master/_documents/images/es/image008.png) 

Figura 2 - Download del *New Reset A.H.I.D.* en formato *ZIP* 

Todo el contenido del archivo deber� ser despaquetado - se recomienda utilizar el aplicativo *WinRar* - y despu�s transportar al servidor web que alojar� el sistema. 

![](https://raw.githubusercontent.com/bireme/proethos/master/_documents/images/es/image010.png) 

Figura 3 - Estructura de archivos 

Se recomienda el envio de los archivos por *FTP* o utilizar la instalaci�n del sistema en directo a trav�s del software del *GitHub* para servidores *Linux*.  

### Crear una base de datos en el servidor *MySQL*  

Crea una base de datos en el servidor *MySQL* con el nombre de *'proethos*' - o el nombre que mejor se adapta al servidor instalado o a los criterios de seguridad de la instituci�n. Los datos de ejemplo en seguida ser�n necesarios para la conexi�n: 

| Requisito      | Valor(ejemplo)  |
| -------------- | --------------- |
| Servidor       | localhost       |
| Base de datos  | xxNameDBxx      |
| Usuario        | sa_xxNameUserxx |
| Contrase�a     | **********      |
| Servidor de BD | MySQL           |


Este archivo solamente ser� creado una vez. Cualquier cambio en los par�metros del sistema, el archivo de configuraci�n deber� ser borrado del sistema por el administrador t�cnico a trav�s del *FTP*. 

El archivo de configuraci�n es creado en el directorio *_db* bajo el directorio ra�z del sistema. 

### Activaci�n de la conexi�n con la base de datos 

En el primero acceso del sistema es necesario tener las configuraciones del archivo de conexi�n con la base de datos. Para que eso pueda occurir, se accede el sistema en su p�gina de instalaci�n a trav�s de cualquier navegador de internet, ej: 
	htttp://localhost:8080/

Si el archivo *_db/db_paho.php* no es localizado, el sistema redirecciona para el area de configuraci�n, presentando la pantalla de la figura 4. 

![](https://raw.githubusercontent.com/bireme/proethos/master/_documents/images/es/image012.png) 

Figura 4 - Pantalla de configuraci�n do archivo *DB* 

En esa pantalla se debe informar el tipo de base de datos (Base Type), con una de las opciones: 
* *MySQL* para se conectar a la base de datos *MySQL* a trav�s del m�todo mysql_connect(), com�n en  na mayor�a de los servidores. 
* *MySQL(PDO)* para acceder la base de datos MySQL utilizando un driver con interfaz PHP Data Objects (PDO). Esa funci�n es utilizada cuando el servidor informa que el m�todo mysql_connect() es obsoleto. 

En el campo *Database host* se debe informar el *IP* o el nombre del servidor de la base de datos. Se puede utilizar *localhost* cuando la base se encuentra en el mismo servidor. 

Los otros campos se refieren a la conexi�n con la base de datos, como el nombre de la base (*Database name*), usuario de conexi�n (*User name*) y la contrase�a (*Password*). En caso de error, el sistema informa en una caja de texto abajo los problema encuentrados. Si todo estuvier configurado correctamente, el archivo *db_paho.php* es creado autom�ticamente, informando el mensaje de �xito. 

### Creaci�n manual del archivo de acceso a la base de datos

Se puede optar por crear el archivo *_db/db_paho.php* manualmente, el caso que no se desea habilitar permisos de escritura para el usuario del *Apache* en esta carpeta. Si es as�, se debe crear el archivo con el contenido abajo, personalizado para cada servidor. Se debe guardar ese archivo en el subdirectorio *_db* con el nombre *db_paho.php*.

```php
 db.php

 <?php
 /* Data Base - Config */
 
 $base='mysql';          /* o mysqlPDO */
 $base_host='localhost'; /* Nombre del host */
 $base_name='xx NameDB xx';  /* Nombre de la base */
 $base_user='root';      /* Usuario */
 $base_pass='password';  /* Contrase�a */

 $ok = db_connect();
 ?>
```

### Inicializar el sistema

En el primer *login* el sistema se encuentra configurado pr�viamente con el usuario y contrase�a abajo:

| Usuario | Contrase�a         |
| ------- | ------------------ |
| admin   | ** xxpasswordxx ** |

Es necesario que al iniciar el sistema tiene que executar en el MEN� del ADMINISTRADOR las funciones Actualizar sistema y Actualizar campos del sistema

## Configurando

### Configuraci�n de los datos de la Comisi�n

(*Texto en producci�n*)

### Actualizaci�n del software

El caso que el sistema fuera instalado utilizando el cliente *GIT*, ser� posible actualizar el software siempre que el repositorio del aplicativo es modificado.

Para realizar la actualizaci�n, accede en la linea de comandos el directorio del aplicativo (ej.: New Reset A.I.H.D.) y escriba:

```
 git pull

```

NOTA: El caso que hubo personalizaci�n en alguna parte del c�digo del aplicativo, el *GIT* informar� que hay una inconsistencia para ejecutar la actualizaci�n. En ese caso, consulte la documentaci�n de *GitHub* para restablecer los archivos que no se deben incluir en la actualizaci�n.



� 2018 New Reset A.I.H.D., Inc.