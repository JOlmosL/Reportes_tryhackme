# Linux Fundamentals

[https://www.notion.so](https://www.notion.so)

### Por: Jesús Olmos

# Linux Fundamentals 1

Link: [https://tryhackme.com/room/linuxfundamentalspart1](https://tryhackme.com/room/linuxfundamentalspart1)

## Task 1: Introducción

Para completar la primera parte, solo basta con darle click al botón verde de “Completed”.

## Task 2: A Bit of Background on Linux

Tenemos que contestar la siguiente pregunta para progresar:

**Research: What year was the first release of a Linux operating system?**

Haciendo un poco de investigación en la web y utilizando el sitio [https://firstmonday.org/ojs/index.php/fm/article/view/1151/1071](https://firstmonday.org/ojs/index.php/fm/article/view/1151/1071) podemos notar que el año de el primer lanzamiento del S.O. de Linux fue en 1991, en septiembre. 

![Untitled](Linux%20Fundamentals%20f6ad001f1e1144c793335d370ad52f8e/Untitled.png)

## Task 3: Interacting With Your First Linux Machine (In-Browser)

Para completar la tercera tarea, deberemos de darle click al botón verde de “Start Machine”, lo cual abrirá una maquina de Linux en nuestro propio navegador.

![Untitled](Linux%20Fundamentals%20f6ad001f1e1144c793335d370ad52f8e/Untitled%201.png)

## Task 4: Running Your First few Commands

Esta cuarta tarea nos pedirá que contestemos dos preguntas utilizando los comandos que aprendimos dentro de la misma tarea, los cuales son:

- echo
    - Nos ayuda para mostrar en pantalla una línea de texto especificada por el usuario
- whoami
    - Muestra en pantalla el nombre del usuario actual

Las preguntas a contestar y para completar la tarea, son:

**If we wanted to output the text "TryHackMe", what would our command be?**

Para mostrar en patalla el texto de “TryHackMe”, utilizaremos el siguiente comando en la consola de Linux:

```bash
echo TryHackMe
```

**What is the username of who you're logged in as on your deployed Linux machine?**

Para conocer el nombre del usuario al cual nos conectamos cuando desplegamos la maquina de linux, será necesario utilizar el siguiente comando dentro de la consola de Linux:

```bash
whoami
```

Lo cual nos mostrará que el usuario actual es: **tryhackme**

![Untitled](Linux%20Fundamentals%20f6ad001f1e1144c793335d370ad52f8e/Untitled%202.png)

## Task 5: Interacting With the Filesystem!

Para completar la quinta tarea, es necesario contestar las siguientes preguntas:

1. On the Linux machine that you deploy, how many folders are there?
2. Which directory contains a file?
3. What is the contents of this file?
4. Use the cd command to navigate to this file and find out the new current working directory. What is the path?

Para contestar la primera pregunta, utilizaremos el siguiente comando para mostrar la cantidad de directorios que hay en el directorio actual:

```bash
ls
```

Podemos observar que hay 4 directorios en el directorio actual. **NOTA:** Si utilizáramos el comando “ls -la” obtendríamos directorios secretos.

Pasando a la segunda pregunta, deberemos de listar el contenido de los directorios que acabamos de encontrar. Para realizar lo anterior, utilizaremos los siguientes comandos:

```bash
ls folder1
ls folder2
ls folder3
ls folder4
```

Veremos que el único folder que contiene un archivo es el directorio “**folder4**”, el cual contiene un archivo llamado “note.txt”, obteniendo la respuesta para la segunda pregunta.

La tercera pregunta consiste en ver el contenido del archivo que encontramos en la pregunta anterior, note.txt. Para ver su contenido, utilizaremos el siguiente comando

```bash
cat folder4/note.txt
```

El contenido del archivo note.txt dentro del directorio folder4 es: “Hello World!”, obteniendo la respuesta para la tercera pregunta.

Por último, para responder a la ultima pregunta, usaremos los siguientes comandos:

```bash
cd folder4
pwd
```

 El último comando nos dar la ruta del directorio actual, siendo esta: “/home/tryhackme/folder4”, obteniendo la respuesta de la cuarta pregunta.

![Untitled](Linux%20Fundamentals%20f6ad001f1e1144c793335d370ad52f8e/Untitled%203.png)

## Task 6: Searching for Files

Esta tarea nos enseñará a utilizar diversos comandos, como lo es:

- find
    - Buscará un archivo específico dentro del directorio actual.
- grep
    - Permite buscar un valor específico dentro de un archivo.
- wc
    - Nos indica el número de líneas que contiene un archivo.

La pregunta que contestaremos para completar la sexta tarea, sera la siguiente:

**Use grep on "access.log" to find the flag that has a prefix of "THM". What is the flag?**

Para contestarla, necesitaremos de utilizar los siguientes comandos:

```bash
ls #Para listar los archivos en el directorio actual, si no se encuentra, usaremos el comando = find -name access.log
grep "THM" access.log
```

El último comando nos regresara la línea en la que encontró el prefijo “THM” perteneciente a la bandera que necesitábamos encontrar, la cuál es: “THM{ACCESS}” 

![Untitled](Linux%20Fundamentals%20f6ad001f1e1144c793335d370ad52f8e/Untitled%204.png)

## Task 7: An Introduction to Shell Operators

La séptima tarea nos enseñará a utilizar los siguientes operadores:

- &
    - Sirve para ejecutar comandos en el segundo plano de la terminal actual.
- &&
    - Permite combinar multiples comandos en una única línea de comandos.
- >
    - Sirve para redirigir, haciendo posible colocar la salida de un comando y dirigirla a otro lado.
- >>
    
    Realiza la misma función que el operador anterior, con la única diferencia de que adjunta en lugar de sobrescribir.
    

Para completar la séptima tarea, deberemos de contestar las siguientes preguntas:

**If we wanted to run a command in the background, what operator would we want to use?**

Si quisiéramos ejecutar un comando en segundo plano, utilizaríamos el operador “&”.

**If I wanted to replace the contents of a file named "passwords" with the word "password123", what would my command be?**

Para reemplazar los contenidos del archivo llamado “passwords” con la palabra “password123”, utilizaríamos el siguiente comando:

```bash
echo password123 > passwords
```

**Now if I wanted to add "tryhackme" to this file named "passwords" but also keep "passwords123", what would my command be?**

Para anexar “tryhackme” al archivo “passwords” manteniendo “passwords123”, utilizaríamos el siguiente comando:

```bash
echo tryhackme >> passwords
```

![Untitled](Linux%20Fundamentals%20f6ad001f1e1144c793335d370ad52f8e/Untitled%205.png)

## Task 8: Conclusions & Summaries

La octava tarea no cuenta con preguntas para responder. Lo que si hace, es dejar en claro los contenidos vistos en **Linux Fundamentals 1**, los cuales fueron:

- Entender porque Linux es tan común el día de hoy.
- Interactuar con tu primera maquina Linux.
- Ejecutar algunos de los comandos más fundamentales.
- Tener una introducción a la navegación por el sistema de archivos y como utilizar comandos como “find” y “grep” para encontrar datos de una manera eficiente.
- Mejorar el conocimiento de comandos al aprender acerca de los operadores importantes de shell.

## Task 9: Linux Fundamentals Part 2

La última tarea nos pide que terminemos con la maquina de Linux que utilizamos y que nos unamos a el enlace para la segunda parte de Linux Fundamentals

[https://tryhackme.com/room/linuxfundamentalspart2](https://tryhackme.com/room/linuxfundamentalspart2)

---

# Linux Fundamentals 2

Link: [https://tryhackme.com/room/linuxfundamentalspart2](https://tryhackme.com/room/linuxfundamentalspart2)

## Task 1: Introduction

Al igual que la primer tarea de Linux Fundamentals 1, solo bastará con que demos clic en el botón verde de “Completed”

## Task 2: Accessing Your Linux Machine Using SSH (Deploy)

Para completar la segunda tarea, será necesario que nos conectemos mediante el protocolo SSH (Secure Shell) a nuestra maquina de tryhackme.

Este protocolo utiliza criptografía para cifrar cualquier entrada del lado del usuario que viaja a través de una red. Eventualmente, será descifrada al llegar a la máquina remota.

Para conectarnos usando ssh, deberemos de utilizar la siguiente sintaxis:

```bash
ssh tryhackme@IP
```

(NOTA: “tryhackme” es el nombre del usuario al cual nos conectaremos.)

Utilizando “tryhackme” de contraseña, lograremos entrar a la máquina de tryhackme mediante el protocolo ssh.

![Untitled](Linux%20Fundamentals%20f6ad001f1e1144c793335d370ad52f8e/Untitled%206.png)

Para terminar con la segunda tarea, solo será necesario que demos clic en el botón verde de “Completed”

## Task 3: Introduction to Flags and Switches

La tercera tarea nos dará una introducción a las banderas que son utilizadas en una gran variedad de comandos de Linux.  Las preguntas que debemos contestar para completar la tarea son las siguientes:

**Explore the manual page of the ls command**

Para completar esta pregunta, solo será necesario que le demos clic al botón verde de “Completed”.

Si seguimos las indicaciones de la pregunta, usaremos el siguiente comando para explorar la página del manual del comando ls:

```bash
man ls
```

Su ejecución nos desplegará lo siguiente:

![Untitled](Linux%20Fundamentals%20f6ad001f1e1144c793335d370ad52f8e/Untitled%207.png)

**What directional arrow key would we use to navigate down the manual page?**

La tecla de la flecha direccional necesaria para navegar hacia abajo en la página del manual sera la de “down” o abajo.

**What flag would we use to display the output in a "human-readable" way?**

La bandera que necesitaríamos para desplegar la salida en una forma “Leible para humanos” será la de -h

![Untitled](Linux%20Fundamentals%20f6ad001f1e1144c793335d370ad52f8e/Untitled%208.png)

## Task 4: Filesystem Interaction Continued

La cuarta tarea nos enseñará a utilizar los siguientes comandos:

- touch
    - Utilizado para crear archivos
- mkdir
    - Crea directorios
- cp
    - Copia archivos o directorios
- mv
    - Mueve archivos o directorios
- rm
    - Remueve (elimina) archivos o directorios
- file
    - Determina el tipo de un archivo

Las preguntas que deberemos de contestar para completar la tarea son las siguientes:

**How would you create the file named "newnote"?**

Para crear e archivo llamado “newnote”, utilizaremos el siguiente comando:

```bash
touch newnote
```

**On the deployable machine, what is the file type of "unknown1" in "tryhackme's" home directory?**

Para conocer el tipo del archivo “unknown1”, utilizaremos el siguiente comando:

```bash
file unknown1
```

La respuesta del comando nos arrojará que el tipo de archivo es ASCII text.

**How would we move the file "myfile" to the directory "myfolder”**

Para mover el archivo “myfile” al directorio “myfolder”, será necesario emplear el siguiente comando:

```bash
mv myfile myfolder
```

**What are the contents of this file?**

Para conocer los contenidos del archivo “myfile”, utilzaremos el siguiente comando:

```bash
cat myfolder/myfile
```

El contenido del archivo “myfile” es: THM{FILESYSTEM}

![Untitled](Linux%20Fundamentals%20f6ad001f1e1144c793335d370ad52f8e/Untitled%209.png)

## Task 5: Permissions 101

La quinta tarea nos dará una introducción a lo que son los permisos, los cuales son esenciales para cualquier archivo y directorio en Linux.

De la misma forma se nos platicará del comando **su**, el cual es utilizado para cambiarnos de usuario.

Las preguntas que contestaremos para completar la quinta tarea son las siguientes:

**On the deployable machine, who is the owner of "important"?**

Para conocer el dueño del archivo important, será necesario que utilicemos el siguiente comando:

```bash
ls -lh
```

El comando nos enlistará los archivos y directorios que se encuentran en el directorio actual junto con información adicional de interés para nosotros, con lo cual sabremos que el dueño del archivo “important” es user2.

**What would the command be to switch to the user "user2"?**

Si quisiéramos cambiarnos al usuario de nombre “user2”, necesitaríamos utilizar el siguiente comando:

```bash
su user2
```

(Nota: Para cambiarnos de usuario, es necesario conocer su contraseña si es que usamos una cuenta con pocos permisos)

**Output the contents of "important", what is the flag?**

Una vez que entramos como “user2”, tendremos acceso al archivo “important”, cuyo contenido es: THM{SU_USER2}

![Untitled](Linux%20Fundamentals%20f6ad001f1e1144c793335d370ad52f8e/Untitled%2010.png)

## Task 6: Common Directories

La sexta tarea nos muestra aquellos directorios comunes de alto interés para nosotros, siendo estos:

- /etc → Almacena archivos que son utilizados por el sistema operativo.
    - En mención especial, hablaremos de los archivos **passwd** y **shadow**, los cuales muestran como tu sistema almacena las contraseñas de los usuarios cifradas en un formato sha512.
- /var → Almacena datos que son frecuentemente accedidos o escritos por servicios o aplicaciones que se encuentran ejecutando en el sistema.
    - como mención especial, podemos decir que en este directorio se encuentran los archivos de **log** y otros datos que no son necesariamente asociados a un usuario específico.
- /root → Es el directorio para el usuario root.
- /tmp → Es un directorio volatil y es utilizado para almacenar datos que solo van a ser accedidos una o dos veces. Una vez que se reinicia la maquina, el contenido de este directorio es vaciado.

Las preguntas que se nos realizan para completar la tarea son los siguientes:

**What is the directory path that would we expect logs to be stored in?**

La direción del directorio que esperaríamos que se utilizara para almacenar los “logs” debería ser: **/var/log**

**What root directory is similar to how RAM on a computer works?**

El directorio raíz que es similar a como funciona una RAM en una computadora es: **/tmp** 

**Name the home directory of the root user**

El nombre del directorio para el usuario raiz es: **/root**

![Untitled](Linux%20Fundamentals%20f6ad001f1e1144c793335d370ad52f8e/Untitled%2011.png)

## Task 7: Conclusions and Summaries

Como tal, no hay preguntas por contestar en la séptima tarea, lo que si tenemos es lo que aprendimos:

- Aprendimos a conectarnos a una maquina Linux de forma remota con SSH
- Avanzamos en nuestro uso de comandos al utilizar banderas y el comando para revisar su manual
- Vimos más comandos que usaremos de manera frecuente para interactuar con el sistema
- Vimos una introducción a los permisos de archivos y al cambio de usuarios
- Terminamos con el conocimiento de los directorios raiz importantes de Linux

## Task 8: Linux Fundamentals Part 3

La última tarea nos pide que terminemos con la maquina de Linux que utilizamos y que nos unamos a el enlace para la tercera parte de Linux Fundamentals:

[https://tryhackme.com/room/linuxfundamentalspart3](https://tryhackme.com/room/linuxfundamentalspart3)

---

# Linux Fundamentals 3

Link: [https://tryhackme.com/room/linuxfundamentalspart3](https://tryhackme.com/room/linuxfundamentalspart3)

## Task 1: Introduction

Al igual que las dos primeras tareas anteriores, solo bastará con que demos clic en el botón verde de “Completed”

## Task 2: Deploy Your Linux Machine

Para completar la segunda tarea, deberemos de iniciar la máquina de tryhackme y conectarnos mediante ssh a la máquina que nos especifica el sitio.

Recordando, para conectarnos usando ssh, deberemos de utilizar la siguiente sintaxis:

```bash
ssh tryhackme@IP
```

![Untitled](Linux%20Fundamentals%20f6ad001f1e1144c793335d370ad52f8e/Untitled%2012.png)

## Task 3: Terminal Text Editors

La tercera tarea nos da una pequeña introducción a dos editores de texto, **nano** y **VIM**.

Para utilizar “nano”, ejecutaremos el siguiente comando:

```bash
nano ARCHIVO
```

Una vez ejecutado, **nano** se desplegará en pantalla. Es bastante sencillo de utilizar y prácticamente todo lo que puedes utilizar se encuentra en la misma pantalla.

Para ejecutar “VIM” deberemos de escribir el siguiente comando:

```bash
vim
```

Entre los beneficios que tenemos por usar vim podemos mencionar:

- Es personalizable
- Realiza énfasis de sintaxis
- Funciona en todas las terminales en donde nano no se encuentre instalado.
- Cuenta con un montón de recursos.

Para completar la tarea, contestaremos la siguiente pregunta:

**Edit "task3" located in "tryhackme"'s home directory using Nano. What is the flag?**

La bandera dentro del archivo “task3” es THM{TEXT_EDITORS}

![Untitled](Linux%20Fundamentals%20f6ad001f1e1144c793335d370ad52f8e/Untitled%2013.png)

## Task 4: General/Useful Utilities

La cuarta tarea nos enseña temas que desglosan información al respecto de como transferir, descargar y guardar archivos.

Para descargar archivos como si accediéramos a ellos a través de nuestro navegador, usamos el comando “wget”, cuya sintaxis es la siguiente:

```bash
wget LINK_TO_FILE.FILE_EXTENSION
```

Para transferir archivos utilizando una copia segura (SCP) utilizando el protocolo ssh, utilizaremos el siguiente comando:

```bash
#Copiando un archivo de nuestra máquina a una máquina remota
scp ARCHIVO_LOCAL.EXTENSION USUARIO@IP:/RUTA/ARCHIVO_TRANSFERIDO.EXTENSION
#Copiando un archivo de una máquina remota a nuestra máquina
scp USUARIO@IP:/RUTA/ARCHIVO_DE_MAQUINA_REMOTA.EXTENSION NUESTRO_ARCHIVO.EXTENSION
```

A través del modulo en python llamado “http.server”, podemos convertir nuestra máquina de Ubuntu en un servidor web, haciendo posible que otros usuarios descargen archivos por medio de los comandos **wget** y **curl**.

 El comando para iniciar un servidor web por medio de python es:

```bash
python3 -m http.server
#Para terminar el servidor, usamos la combinación de teclas "Ctrl + c"
```

Las preguntas que deberemos contestar para completar la tarea son las siguientes:

**Now, use Python 3's "HTTPServer" module to start a web server in the home directory of the "tryhackme" user on the deployed instance.**

Para inicializar nuestro servidor HTTP pode medio de python3 en nuestro usuario “tryhackme”, usaremos el siguiente comando:

```bash
python3 -m http.server
```

**Download the file http://MACHINE_IP:8000/.flag.txt onto the TryHackMe AttackBox. What are the contents?**

Para descargar el archivo “.flag.txt” en nuestra máquina local de TryHackMe, usaremos el siguiente ocmando:

```bash
wget http://IP_DE_LA_MAQUINA_REMOTA/.flag.txt
```

Al ejecutar un comando “cat”, vemos que el archivo contiene: THM{WGET_WEBSERVER}

![Untitled](Linux%20Fundamentals%20f6ad001f1e1144c793335d370ad52f8e/Untitled%2014.png)

## Task 5: Processes 101

La quinta tarea nos da un recorrido a través del mundo de los programas que se encuentran ejecutando en la máquina de Linux llamados procesos.

Para ver los procesos que se encuentran ejecutando dentro de nuestra sesión de usuario, al igual que información adicional de ellos, utilizamos el siguiente comando:

```bash
ps
```

Si quisiéramos ver la lista de los procesos ejecutados por otros usuarios y aquellos pertenecientes al sistema, le anexaremos la palabra “aux” al comando anteriormente visto.

```bash
ps aux
```

Otro comando de utilidad, el “top”, el cual muestra estadísticas en tiempo real sobre los procesos que se encuentran corriendo en el sistema.

Existen multiples formas de terminar los procesos, entre ellas, tenemos el uso del comando “kill”. De la misma forma, existen otros comandos especializados para terminar un proceso como lo es:

- SIGTERM → Mata el proceso permitiendo que se ejecuten tareas de limpieza antes de que se termine el proceso
- SIGKILL → Mata el proceso sin permitir que se ejecuten las tareas de limpieza
- SIGSTOP → Detiene o suspende al proceso

```bash
kill PROCESS_ID
kill -sigterm PROCESS_ID
kill -sigkill PROCESS_ID
kill -sigstop PROCESS_ID
```

No todos son procesos, si no que también existen formas de interactuar co servicios o aplicaciones que se trabajan en cuanto se enciende el sistema.

Por medio del comando “systemctl” podemos interactuar con **systemd** process/daemon. Su sintaxis es la siguiente:

```bash
systemctl start SERVICE
systemctl stop SERVICE
systemctl enable SERVICE
systemctl disable SERVICE
```

Habíamos visto con anterioridad el uso de la bandera “&” para ejecutar programas en segundo plano. Si ejecutamos un programa en segundo plano podremos ver el pid de su proceso.

Otra forma de emplear la ejecución en segundo plano es si usamos la combinación de teclas “Ctrl + z.”

Si no queremos que el programa se encuentre en ejecución en segundo plano, usaremos el comando “fg”

```bash
fg
```

Las preguntas que debemos de contestar para completar la tarea, son las siguientes:

**If we were to launch a process where the previous ID was "300", what would the ID of this new process be?**

Dado que los IDs de los procesos son autoincrementales, el valor del nuevo proceso será de 301.

**If we wanted to cleanly kill a process, what signal would we send it?**

Para terminar un proceso de una maneraa “limpia”, deberemos de emplear el comando “sigterm”.

```bash
kill -sigterm PROCESS_ID
```

**Locate the process that is running on the deployed instance (MACHINE_IP). What flag is given?**

Para localizar el proceso que se encuentra ejecutándose en nuestra máquina actual, usaremos el siguiente comando:

```bash
ps aux
```

Tras analizar la lista de los procesos, podemos ver que existe un proceso con una sintaxis muy parecida a la de las banderas encontradas anteriormente, siendo esta: THM{PROCESSES}

**What command would we use to stop the service "myservice"?**

El comando que usaremos para detener el servicio “myservice” sera el siguiente:

```bash
systemctl stop myservice
```

**What command would we use to start the same service on the boot-up of the system?**

El comando que se requiere para iniciar el mismo servicio (myservice) al encender el sistema es el siguiente:

```bash
systemctl enable myservice
```

**What command would we use to bring a previously backgrounded process back to the foreground?**

El comando utilizado para traer un proceso enviado con anteriedad a el fondo (segundo plano), es “fg”

![Untitled](Linux%20Fundamentals%20f6ad001f1e1144c793335d370ad52f8e/Untitled%2015.png)

## Task 6: Maintaining Your System: Automation

La sexta tarea nos habla acerca de el proceso **cron**, el cual puede utilizarse para programar acciones o tareas que tomen lugar tras encender el sistema por medio de **crontabs**.

Una crontab es un archivo con un formato reconocido por el proceso **cron** para ejecutar cada línea paso a paso. Dentro del archivo se especifican valores de tiempo.  

Las crontabs pueden ser editadas usando el siguiente comando:

```bash
crontab -e
```

La única pregunta que debemos contestar para completar la tarea es la siguiente:

**When will the crontab on the deployed instance (MACHINE_IP) run?**

Para conocer que crontab sera ejecutada en la máquina actual, ejecutaremos el siguiente comando:

```bash
crontab -e
```

Tras su ejecución, veremos que existe un crontab llamado @reboot, siendo este la respuesta.

![Untitled](Linux%20Fundamentals%20f6ad001f1e1144c793335d370ad52f8e/Untitled%2016.png)

## Task 7: Maintaining Your System: Package Management

La séptima tarea no cuenta con preguntas para superarla, pero si nos proporciona información valiosa acerca de no solo de Repositorios de Paquetes y Software sino también de como administrar los repositorios.

Software desarrollado por la comunidad será subido a un repositorio llamado “**apt**”.  Podemos utilizar el comando **ls** dentro del directorio “/etc/apt” para ver todas aquellas herramientas en nuestro sistema.

Si quisiéramos agregar repositorios, utilizaríamos el siguiente comando:

```bash
add-apt-repository
```

 El comando “apt” contiene herramientas que nos permitirán administrar paquetes y fuentes de software.

```bash
apt update SOFTWARE
apt install SOFTWARE
apt remove SOFTWARE
```

## Task 8: Maintaining Your System: Logs

La octava tarea nos enseña la importancia de los “logs” dentro de nuestro sistema Linux en el directorio **/var/log.**

Estos archivos nos ayudan a monitoriear la lslaud del sistema y a protegerlo.

Existen dos tipos de archivos log de alto interés, siendo estos:

- access
- error

Estos “logs” almacenan información de como se ejecuta el sistema operativo, y las acciones que realizan usuarios.

Para completar la tarea, será necesario responder a las siguientes preguntas:

**Look for the apache2 logs on the deployable Linux machine**

El directorio de “apache2” que contiene archivos logs se encuentra dentro del directorio /var/log.

**What is the IP address of the user who visited the site?**

La dirección IP que se obtiene del usuario que visito el sitio se puede obtener al accesar por medio del comando “cat” al archivo “access.log”. Al leer el archivo, vemos que la IP del usuario que intento acceder es: 10.9.232.111

**What file did they access?**

Para concer el archivo al que accedieron, ocuparemos el comando “cat” para acceder al archivo “access.log.1”, con el cual sabemos que accedieron al archivo: catsanddogs.jpg

![Untitled](Linux%20Fundamentals%20f6ad001f1e1144c793335d370ad52f8e/Untitled%2017.png)

## Task 9  Conclusions & Summaries

Como ya es costumbre en este punto, no hay preguntas por contestar en la novena tarea, lo que si tenemos es un resumen de lo aprendido:

- Utilizar editores de texto
- Conocimiento de utilidades generales como lo es contenidos de descarga y servicio a traves de python
- Una introducción a los procesos
- A mantener y automatizar el sistema mediante crontabs

De la misma forma, nos recomiendan más cuartos, siendo estos:

- Bash Scripting - [https://tryhackme.com/room/bashscripting](https://tryhackme.com/room/bashscripting)
- Regular Expressions - [https://tryhackme.com/room/catregex](https://tryhackme.com/room/catregex)