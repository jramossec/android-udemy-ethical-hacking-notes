# 4. Comandos básicos de Linux

Vamos a ver los comandos básicos de Linux para poder movernos en la terminal y ejecutar comandos.

Es fundamental saber moverse en este tipo de entornos porque no todo es gráfico.

## ls

```bash
ls
```

Es para listar las carpetas que tenemos.

## cd (change directory)

El comando `cd` es para cambiar de directorio. Ejemplo:

```bash
cd HiddenEye
ls
```

Y listamos el contenido de ese directorio.

Si nosotros queremos movernos al directorio anterior, a la carpeta anterior, lo que hacemos es:

```bash
cd ..
ls
```

## cat (catenate)

Es para listar el contenido de un archivo:

```bash
cd HiddenEye
ls
cat HiddenEye.py
```

Veremos el código Python de este archivo.

Hacemos:

```bash
cd ..
ls
```

## nano

>Nano es un editor de textos, nos permite crear archivos y editarlos

Vamos a crear un archivo de texto:

```bash
nano Archivodetexto.txt
```

Pero primero, debemos instalar `nano` en **Termux**:

```bash
pkg install nano
```

Y podemos poner cualquier cosa en el archivo de texto:

```plaintext
hola soy un archivo de texto
```

Para salir de `nano`, hacemos **Ctrl + O** y **Enter** para guardar, y **Ctrl + X**.

Y para ver el contenido de este contenido de texto, hacemos:

```bash
$ cat Archivodetexto.txt
hola soy un archivo de texto
```

## rm (remove)

Para eliminarlo, hacemos:

```bash
ls
rm Archivodetexto.txt
ls
```

Ya no tenemos el archivo de texto.

## mkdir (make directory)

Es para crear una carpeta:

```bash
mkdir Carpeta
ls
```

Apareció el nuevo directorio llamado `Carpeta/`.

## rmdir (remove directory)

Y para eliminar el directorio:

```bash
rmdir Carpeta/
ls
```

Ya no tenemos la carpeta `Carpeta/`.

## pwd (print working directiry)

Hacemos:

```bash
cd HiddenEye/
ls
cd Server/
ls
cd www/
```

Para saber en que directorio estamos, en que carpetas estuvimos navegando:

```bash
pwd
```

```bash
$ pwd
/data/data/com.termux/files/home/HiddenEye/Server/www
```

Hacemos:

```bash
cd ..
cd ..
cd ..
pwd
ls
```

Estamos en el directorio `home/`, en el directorio anterior:

```bash
$ pwd
/data/data/com.termux/files/home
```

## clear

Para eliminar los comandos que estuvimos poniendo (Linux):

```bash
clear
```

Y borramos todo.

En una consola **cmd** de Windows, **PowerShell**:

```powershell
cls
```

## whoami

Para ver que usuario somos:

```bash
whoami
```

```bash
$ whoami
u0_a57
```

Si sale `root`, es porque somos usuario `root`.

## uname

Para ver la versión de Termux:

```bash
uname -r
```

```bash
$ uname -r
4.9.31
```

Para ver el entorno en el que estamos corriendo:

```bash
uname -a
```

```bash
$ uname -a
Linux localhost 4.9.31 #1 SMP PREEMPT Jan 13 07:17:31 IST 2021 i686 Android
```

Si queremos hacer un *Pentesting* y ver el equipo que estamos atacando, podemos poner este tipo de comandos:

```bash
whoami
uname
```

>Utilizar el comando uname también nos sirve para obtener la versión del sistema a la hora de escalar privilegios.