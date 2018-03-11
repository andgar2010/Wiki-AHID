## INSTALACIÓN

### Download del sistema

Hay dos modos para se instalar el sistema:

* con versionamiento \(git\);

* sin versionamento \(zip\).

#### Instalación a través de cliente_GIT_\(versionamiento\)

Ese es el modo preferible para se instalar el sistema, porque se permite actualizar el aplicativo en modo simple y seguro, y también manteniendo las personalizaciones privadas, configuraciones generales del sistema etc.

Para instalar el sistema por el cliente del_GIT_, escriba en la linea de comandos de_Linux_- bajo el directorio donde se desea instalar el paquete - el comando abajo:

git clone git://github.com/bireme/proethos.git proethos

#### Instalación por paquete zip

Para descargar la última versión del sistema New Reset A.H.I.D. acceda el enlace

```
https://github.com/andgar2010/Project_New_Reset_AIHD
```

y haga un clic en el icono “Download ZIP” que se encuentra al lado derecho de la página.

![](https://raw.githubusercontent.com/bireme/proethos/master/_documents/images/es/image007.png)

Figura 1 - Icone para_Download_

Después del clic el sitio de GitHub proporcionará el paquete de la última versión para ser guardado en su computadora.

![](https://raw.githubusercontent.com/bireme/proethos/master/_documents/images/es/image008.png)

Figura 2 - Download del_New Reset A.H.I.D.\_en formato\_ZIP_

Todo el contenido del archivo deberá ser despaquetado - se recomienda utilizar el aplicativo_WinRar_- y después transportar al servidor web que alojará el sistema.

![](https://raw.githubusercontent.com/bireme/proethos/master/_documents/images/es/image010.png)

Figura 3 - Estructura de archivos

Se recomienda el envio de los archivos por_FTP\_o utilizar la instalación del sistema en directo a través del software del\_GitHub\_para servidores\_Linux_.

### Crear una base de datos en el servidor_MySQL_

Crea una base de datos en el servidor_MySQL\_con el nombre de_'proethos\_' - o el nombre que mejor se adapta al servidor instalado o a los criterios de seguridad de la institución. Los datos de ejemplo en seguida serán necesarios para la conexión:

| Requisito | Valor\(ejemplo\) |
| :--- | :--- |
| Servidor | localhost |
| Base de datos | xxNameDBxx |
| Usuario | sa\_xxNameUserxx |
| Contraseña | **\*\*** |
| Servidor de BD | MySQL |

Este archivo solamente será creado una vez. Cualquier cambio en los parámetros del sistema, el archivo de configuración deberá ser borrado del sistema por el administrador técnico a través del_FTP_.

El archivo de configuración es creado en el directorio\_\_db\_bajo el directorio raíz del sistema.

### Activación de la conexión con la base de datos

En el primero acceso del sistema es necesario tener las configuraciones del archivo de conexión con la base de datos. Para que eso pueda occurir, se accede el sistema en su página de instalación a través de cualquier navegador de internet, ej:

```
htttp://localhost:8080/
```

Si el archivo\_\_db/db\_paho.php\_no es localizado, el sistema redirecciona para el area de configuración, presentando la pantalla de la figura 4.

![](https://raw.githubusercontent.com/bireme/proethos/master/_documents/images/es/image012.png)

Figura 4 - Pantalla de configuración do archivo_DB_

En esa pantalla se debe informar el tipo de base de datos \(Base Type\), con una de las opciones:

* \_MySQL\_para se conectar a la base de datos\_MySQL\_a través del método mysql\_connect\(\), común en na mayoría de los servidores.

* \_MySQL\(PDO\)\_para acceder la base de datos MySQL utilizando un driver con interfaz PHP Data Objects \(PDO\). Esa función es utilizada cuando el servidor informa que el método mysql\_connect\(\) es obsoleto.

En el campo\_Database host\_se debe informar el\_IP\_o el nombre del servidor de la base de datos. Se puede utilizar\_localhost\_cuando la base se encuentra en el mismo servidor.

Los otros campos se refieren a la conexión con la base de datos, como el nombre de la base \(_Database name_\), usuario de conexión \(_User name_\) y la contraseña \(_Password_\). En caso de error, el sistema informa en una caja de texto abajo los problema encuentrados. Si todo estuvier configurado correctamente, el archivo\_db\_paho.php\_es creado automáticamente, informando el mensaje de éxito.

### Creación manual del archivo de acceso a la base de datos

Se puede optar por crear el archivo_\_db/db\_paho.php\_manualmente, el caso que no se desea habilitar permisos de escritura para el usuario del\_Apache\_en esta carpeta. Si es así, se debe crear el archivo con el contenido abajo, personalizado para cada servidor. Se debe guardar ese archivo en el subdirectorio_\_db_con el nombre\_db\_paho.php_.





© 2018 New Reset A.I.H.D., Inc.

