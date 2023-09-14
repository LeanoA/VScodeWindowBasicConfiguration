# Configuracion basica VS Code

## Introducción

Este repositorio contiene una configuración básica para usar VS Code con C++ en Windows. Utiliza MSYS2 intalado por CodeBlock en su carpeta local.
Este repositorio esta orientado a estudiantes que comienzan a programar en C++ y comenzaron a utilizar CodeBlock por simplicidad pero desean utilizar VS Code.

## Instalación	

Se asume que se descargo e instaló `CodeBlock` con `MSYS2` (para simplificar la instalación) y `VS Code` en su versión mas reciente.

`MSYS2` es una shell minimalista de linux/unix para Windows. Se utiliza para compilar y debuggear el código C++.

En el repositorio, dentro de la carpeta `.vscode` se encuentra el archivo `task.json` y `launch.json` como ejemplo.


## Comando utiles

Para verificar la instalación de `g++` y `gdb` se puede utilizar los siguientes comandos en la consola:

```bash
g++ --version
gdb --version
```
Aunque la instalación de `MSYS2` debería agregar los comandos a la variable de entorno `PATH` de Windows, se puede agregar manualmente.

## Add the Directory to the Path of the Environment Variables

If you use a 64 -bit operating system like me, access the Mingw64 folder.
In my case `C:\msys64\mingw64\bin` and copy the direction.

Open in windows `Edit the system environment variables`
- click `Environment Variables` from the Advanced tab.
- Click on the `PATH` and select it.
- Then click `Edit`. 
- Click `New`. An empty field is displayed. Paste the directory here.

## Using g++ and gdb with VScode

Select g++ compiler.

- Check or modify `miDebuggerPath` line in `lauch.json` file: `"miDebuggerPath": "C:\\Program Files\\CodeBlocks\\MinGW\\bin\\gdb.exe"`

- Check or modify `command` line in `task.json` file: `"command": "C:\\Program Files\\CodeBlocks\\MinGW\\bin\\g++.exe",`

For more information, visit https://code.visualstudio.com/docs/languages/cpp.

## Reference
Original guide from https://gist.github.com/roblogic/b401aa68d0a7c7c96095fa64a7c9f684
Othe reference https://www.freecodecamp.org/news/how-to-install-c-and-cpp-compiler-on-windows/

## Disclaimer

This document is provided for information only, no guarantees. I have no association with MSYS2 or related projects.
