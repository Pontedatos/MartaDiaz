# Registro del proceso de aprendizaje 

### A continuación se presentan las nociones elementales adquiridas a lo largo del cuatrimestre en la asignatura de Periodismo de Datos, siguiendo para su estructura el esquema/índice proporcionado por el profesor en Aula Global. 

> NOTA: al trabajar con un ordenador de Apple, algunos de los procesos han sido, en mi caso, diferentes a los de las compañeras que trabajan con Windows. Al ser estas últimas la mayoría en el conjunto de la clase, de forma inevitable los apuntes atienden más a su circunstancia. No obstante, se intentará —en la medida de lo posible— adaptar la explicación del proceso de aprendizaje al uso de un Mac o, en su defecto, reflejar cómo se ha procedido en el caso de trabajar desde Windows. 

## Instalación de un programa de emulación de la terminal

Para esta primera aproximación a la asignatura, las usuarias de Windows tuvieron que descargarse Cygwin y/o Ubuntu. En el caso de Mac, la Terminal está presente por defecto en todas las versiones de OS X. Se trata del programa por el que el usuario accede a UNIX, es decir, la base sobre la que se escribe el sistema operativo de Apple. La Terminal en Mac se sitúa dentro de la carpeta de “Aplicaciones”. 

En mi caso, los pasos a seguir consistían en la descarga y activación de XCode. Antes de proceder a la descarga, actualicé el sistema operativo de mi portátil. Concluido este paso, ejecuté el comando `xcode-select --install` en la Terminal. 


## Configuración del programa (o trabajando en la terminal)

A sabiendas del uso recurrente que haríamos de la Terminal, el profesor quiso introducirnos en el lenguaje propio y presentarnos algunas operaciones que facilitarían y agilizarían el trabajo en la Terminal. De nuevo, al ser usuaria de Mac no fue necesario llevar a cabo alguna de las configuraciones que sí realizaron mis compañeras.

### Exploración de los directorios

Aprendimos el comando `cd` (*change directory*), con el que modificamos nuestra posición dentro de un conjunto de archivos; es decir *nos movemos* por las carpetas hasta situarnos dentro de aquella desde la que queremos seguir trabajando. Empleando dicho comando llegamos, desde la terminal, a la carpeta de la asignatura que cada cual había creado de la forma convencional (o por nosotras conocida hasta hace apenas unos meses). 

A fin de ahorrar tiempo y trabajo en esta tarea de explicitación de la ruta de nuestra carpeta, existe la posibilidad de crear un comando que nos conduzca directamente a la misma sin necesidad de rastrear todo el árbol de directorios. Serían los comandos `micasa` o `home` , pero solo se han establecido para las usuarias de Windows. 

### Nociones básicas de la terminal

En las primeras aproximaciones, y precisamente para responder a las preguntas que todas nos hacíamos dado nuestro desconocimiento, aprendimos las operaciones más sencillas para entender nuestra identidad y posición en la Terminal: 

- `whoami` (*Who am I?*): imprime el nombre del usuario actual en el momento en que se invoca

- `pwd` (*print workind directory*): devuelve la ruta en la que estamos situados. Es uno de los comandos más importantes. 

Aunque pudiera parecer una cuestión menor, lo recojo aquí por ser una utilidad que desconocíamos y que desde luego facilita el trabajo en la terminal: la tecla tabuladora. 

### GitHub

Momento de vincular el repositorio creado vía online en GitHub con una carpeta en nuestro ordenador personal, de forma tal que los cambios realizados en nuestro archivo local se añadan también al repositorio en línea. 

Clonamos el repositorio en el ordenador, copiando para ello el enlace desde Github (botón verde “Code”) y ejecutando en la terminal el comando `git clone *incluir-aquí-enlace*`. Es importante hace esto desde la carpeta donde queramos guardar el repositorio vinculado (es decir, asegurarnos mediante `pwd` de estar en el sitio correcto, y si no es así, movernos con `cd`). 

Para vincular los cambios debemos configurar el usuario y correo de GitHub en la terminal. Usamos para ello dos comandos: 

- `git config --global user.name nuestro-nombre-usuario`
- `git config --global user.mail nuestro-correo-github`

Una vez completada la configuración, ya sería posible empezar a trabajar con GitHub desde la terminal. El proceso de vinculación de los archivos se realiza en tres sencillos pasos: 

1.	`git add . ` añade los cambios de archivo en el directorio.
2.	`git commit .` para comitear.
3.	`git push` para enviar los cambios al repositorio en GitHub. 

Además de estos tres elementales, existen otros comandos muy útiles. El primero de ellos, `git status`, nos aporta información sobre el estado en el que se encuentra el directorio de trabajo (los cambios que se han iniciado y faltan por comitear, etc.). Por su parte, `git pull` permite actualizar el repositorio local con el contenido del remoto (es decir, actualiza en el ordenador los cambios que se han realizado en la nube). 


## Configuración de un programa de edición de texto

La edición de texto desde la terminal se ha llevado a cabo con nano. Para ello se ha procedido a su instalación con `brew install nano`. Las compañeras de Windows configuraron el editor para conseguir ajustar el texto a la pantalla y numerar las líneas (en mi caso, no tengo nano configurado de esa forma, pero desconozco si se debe a una cuestión de incompatibilidad con Mac). En cualquier caso, habría que ejecutar `nano $HOME/.nanorc` y escribir a continuación lo siguiente: 

`# Ajustar el texto a pantalla`
`set softwrap`
`# Numerar las líneas`
`set linenumbers`

Guardamos los cambios con `Ctrl + O` o salimos del archivo haciendo `Crtl + X` (se nos preguntará si queremos guardar igualmente). 


## Configuración y funcionamiento de un gestor de paquetes/programas del emulador de la terminal 
El gestor o administrador de paquetes más popular para Mac OS X es Homebrew. Para su instalación se copió lo siguiente en la terminal: `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
## Versión del lenguaje de SHELL utilizado
Bash es el Shell pretederminado en macOS, pero desde la propia terminal se ofrece la posibilidad al usuario de pasar a `zsh` , ejecutando para ello `chsh -s /bin/zsh`. En mi caso, este cambio no ha sido realizado, como puede comprobarse al ejecutar `echo $SHELL`, pues la respuesta obtenida es “/bin/bash”. La versión específica de Bash puede conocerse por dos vías: `$SHELL –versión`o `bash --version`. La respuesta obtenida en uno y otro caso es: GNU bash, version 3.2.57. 
## Valor de la variable de entorno PATH 
PATH es una de las variables de entorno más importantes para ejecutar comandos. En primer lugar, hay que recordar que todas las variables empiezan con el símbolo `$`, o lo que es lo mismo, se invocan con él. Podemos ver las variables de esta forma: `$PATH`. Si consultar el valor de la variable usamos `echo` :`echo $PATH`.
## Comandos utilizados y ejemplos.
A lo largo de este resumen ya se han ido introduciendo varios comandos, pero se presentan a continuación algunos de los que no han sido presentados todavía: 
- `cat` para concatenar archivos. 
- `ls` lista los archivos o directorios que hay en el espacio de trabajo en el que nos encontramos. Por ejemplo, si ejecuto este comando en mi carpeta MartaDiaz, se imprimirían en pantalla todos los archivos relativos a las prácticas de la Asignatura de Periodismo de Datos. 
- `-l` similar al anterior, pero con información más extendida. 
- `man` seguido de un comando cualquier sirve para abrir el manual de dicho comando; es decir, explica en qué consiste y cómo funciona. Para salir del `man` usamos la `q` .
- Barra vertical `|` , llamada tubería, envía el resultado de un programa a otro programa (man ls | less). 

- `>` (mayor que) envía la salida del comando que le precede a donde nosotros le indiquemos. 

- `>>` (dos mayor que) lo envía al final, si existe; y si no existe, lo crea. 

- `env` para ver todas las variables de entorno. 

- `mkdir` para crear un repositorio. Por ejemplo, si quisiéramos crear una carpeta en la que almacenar todos los repositorios de GitHub, haríamos `mkdir github` . Si queremos crear el directorio y entrar en la carpeta de una vez, ponemos las órdenes seguidas pero separadas por dos `&&`  (ejecuta dos comandos en una misma línea). En este caso: `mkdir github && cd github`. 

- `cp` , seguido de origen y del destino, para copiar.
- `mv` para mover o renombrar. 

- `grep` para buscar palabras dentro de archivos de texto desde la terminal. 

- `cat .bash_history` para ver el historial de comandos. 

- `touch [nombrearchivo]` para crear un archivo nuevo. Por ejemplo, si queremos crear un README.md en nuestra carpeta, escribimos `touch README.md` .
- `wget [enlace]` para descargarnos un archivo/contenido de una web. 
