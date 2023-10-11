# Linux Fundamentals

### Por: Jesús Olmos Larios

# Linux Fundamentals 1

Link: [https://tryhackme.com/room/linuxfundamentalspart1](https://tryhackme.com/room/linuxfundamentalspart1)

## Task 1: Introducción

Para completar la primera parte, solo basta con darle click al botón verde de “Completed”

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