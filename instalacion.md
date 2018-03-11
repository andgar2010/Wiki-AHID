
### Download del sistema
### Descarga el instalador del sistema

Hay dos modos para se instalar el sistema:



#### Instalación a través de cliente *GIT* (versionamiento)




#### Instalación por paquete zip

Para descargar la última versión del sistema New Reset A.H.I.D. acceda el enlace







Figura 2 - Download del *New Reset A.H.I.D.* en formato *ZIP*



Figura 3 - Estructura de archivos


### Crear una base de datos en el servidor_MySQL_
### Crear una base de datos en el servidor *MySQL*


| Requisito      | Valor (ejemplo) |
| :------------- | :-------------- |
| Servidor       | localhost       |
| Base de datos  | xxNameDBxx      |
| Usuario        | sa_xxNameUserxx |
| Contraseña     | ********        |
| Servidor de BD | MySQL           |
| Requisito      | Valor (ejemplo)  |
|----------------|------------------|
| Servidor       | localhost        |
| Base de datos  | xxNameDBxx       |
| Usuario        | sa_xxNameUserxx  |
| Contraseña     | \*\*\*\*\*\*\*\* |
| Servidor de BD | MySQL            |



### Activación de la conexión con la base de datos










### Creación manual del archivo de acceso a la base de datos


db.php

 <?php
 /* Data Base - Config */
 $base='mysql';          /* o mysqlPDO */
 $base_host='localhost'; /* Nombre del host */
 $base_name='proethos';  /* Nombre de la base */
 $base_user='root';      /* Usuario */
 $base_pass='password';  /* Contraseña */

 $ok = db_connect();
 ?>

[^1]: Copyright.
[^ref1]: 
© 2018 New Reset A.I.H.D., Inc.

Here is a footnote reference,[^1] and another.[^2]

[^1]: © 2018 New Reset A.I.H.D., Inc.

[^2]: Here's one with multiple blocks.

​ Subsequent paragraphs are indented to show that they belong to the previous
footnote.

Here is an inline note.[^3]

[^3]: Inlines notes are easier to write, since you don't have to pick an
identifier and move down to type the note.

---
&copy; My Company, 2018;
