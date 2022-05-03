# Metodología 

## ¿Cómo se ha creado la página web? 

### Creación del repositorio

El primer paso ha consistido en crear un nuevo repositorio, esta vez desde la organización Pontedatos, en la que nos encontramos todas las alumnas de la asignatura. El repositorio creado desde la pestaña “New” lleva mi nombre (pero respetando las normas de no incluir espacios y prescindir de las tildes): MartaDiaz. Completado este sencillo paso inicial, la siguiente operación consistió en vincular este nuevo repositorio con la terminal personal. Para llevar a cabo esta vinculación se empleó la función `git clone` seguida del enlace del repositorio recién creado. 

Dicho repositorio, por supuesto, se encuentra vacío. Será necesario copiar todas las prácticas realizadas a lo largo del cuatrimestre, y que de momento se encuentran almacenadas en el repositorio personal. El comando `cp` nos permite realizar esta copia. 

Incluidos todos los archivos en el nuevo repositorio, se procede a modificar `README.md`, que ahora debe ser mucho más extenso e incluir un índice de todas las prácticas con sus respectivos enlaces de acceso. Para ello acudimos a `nano` . Una vez abierto el archivo, borramos el texto previamente escrito e introducimos la actualización pertinente. Guardamos los cambios antes de cerrar haciendo `Crtl + X` . Se nos preguntará si queremos guardar, y confirmaremos pulsando la tecla `S` . Llegados a este punto ya se ha “rellenado” la carpeta del ordenador con los archivos del curso y el `README.md` que los recopila, pero estos cambios no figuran todavía en GitHub. 

### Subir los archivos al repositorio en GitHub

Esta tarea se divide en tres pasos fundamentales: 

1.	El comando `git add .` para añadir los archivos. 
2.	El comando `git commit .` para guardar los cambios
3.	El comando `git push` para “empujar” los archivos hacia GitHub. En ocasiones este paso requiere de un *token* (contraseña proporcionada por GitHub); en mi caso particular y en esta ocasión no ha sido necesario. 

Si en la ejecución de estos tres pasos se produjera algún inconveniente, el comando `git status` suele ser de gran ayuda al indicarnos cuál es la situación actual de nuestro repositorio. También el comando `git pull` resulta de gran utilidad cuando necesitamos fusionar los cambios. 

### Creación de la página
Desde el repositorio creado en GitHub, hacemos *click* en Settings. Se activará la opción de Pages. Seleccionamos la rama main y la carpeta /root. Una vez se guardan los cambios (*save*), se genera una url que debemos incluir en la descripción del repositorio en Pontedatos. Cabe mencionar que es normal que la página web tarde algunos segundos (o minutos) en actualizarse. 
De forma automática, GitHub convierte el archivo `README.md` en `html` , de forma tal que el índice de prácticas que hemos configurado al inicio desde nano —con enlaces— será el contenido mismo de nuestra página web
