# 3. Instalando dependencias

Vamos a ver a cómo instalar dependencias en **Termux** para correr las herramientas correctamente.

## Primer comando

Para actualizar los paquetes del emulador:

```bash
pkg update
pkg upgrade
```

Similar a cuando actualizamos los paquetes en Kali Linux.

## Instalar Python

```bash
pkg install python
```

Esto para poder correr las herramientas de hacking.

## Instalar Git

```bash
pkg install git
```

Esto para poder clonar repositorios.

## Actualizar el administrador de paquetes de Python

```bash
pip install --upgrade pip
```

>**NOTA:** Esto dará error, ya que Termux bloque la actualización porque puede romper la integración con Termux. Se actualiza automáticamente al
>hacer `pkg update && pkg upgrade`.

## Instalar y actualizar pip2

```bash
pkg install python2
pip2 install --upgrade pip
```

Hay herramientas que utilizan *Python2* y otras *Python3*.

>**NOTA:** Este no da error al actualizar pip2.

## Instalar PHP

```bash
pkg install php
```

Las herramientas de pishing utilizan PHP para poder crear el servidor y poder realizar el ataque de phishing correctamente.