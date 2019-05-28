---
title: Instalando Unlaunch
layout: single
sidebar:
  nav: "side"
---

¡Antes de empezar, deberías comprobar si tu tarjeta SD tiene errores mediante [Comprobación de SD](/guia_dsi/anexo/comprobación-de-sd)!
{: .notice--warning}

¡Antes de empezar, se recomienda que los usuarios de Windows habiliten la opción para mostrar extensiones de archivo mediante [Extensiones de archivo (Windows)](/guia_dsi/anexo/extensiones-de-archivo-(windows))!
{: .notice--info}

Esta guía está destinada a la instalación de Unlaunch, HiyaCFW y TWiLight Menu++ en un DSi *sin modificar*. Si buscas instalar TWiLight Menu++ en un 3DS o 2DS *ya modificado*, sigue [Instalando TWiLight Menu++ en 3DS](/guia_dsi/anexo/instalando-twilight-menu++-3ds).
{: .notice--primary}

___

Unlaunch es un explit de arranque para DSi que te permitirá instalar HiyaCFW, un custom firmware para DSi, en tu consola.

## Descargas

- La última versión de [Unlaunch](https://problemkaputt.de/unlaunch.zip)
- La última versión de [HBMenu](https://github.com/devkitPro/nds-hb-menu/releases/latest){:target="_ blank"}
- La última versión de [Memory Pit](https://gbatemp.net/attachments/pit-zip.168232/)
- La última versión de [fwTool](/guia_dsi/archivos/fwTool.nds)

## Preparando la tarjeta SD

1. Inserta tu tarjeta SD en tu ordenador.
2. Copia el archivo `pit.bin` a la carpeta `private/ds/app/484E494A` de tu tarjeta SD.
  - Si la carpeta no existe créala.
3. Copia el archivo `BOOT.NDS` de la carpeta `hbmenu` del archivo `.tar.bz2` de HBMenu a la raíz de tu tarjeta SD.
4. Copia el archivo `.DSI` del archivo `.zip` de Unlaunch a la raíz de tu tarjeta SD y renómbralo a `unlaunch.nds`.
  - Si te pregunta si quieres cambiar la extensión del archivo presiona Aceptar.
5. Copia el archivo `.nds` de fwTool a la raíz de tu tarjeta SD.
6. Saca la tarjeta SD de tu ordenador y vuélvela a introducir en tu DSi.

## Creando una copia de la NAND

1. Abre la aplicación Cámara Nintendo DSi.
2. Presiona `Tarjeta SD`.
3. Toca `Álbum`.
  - Esto debería lanzar HBMenu.
4. Navega a `fwtool.nds` y luego presiona (A).
  - fwTool debería aparecer.
5. Navega a `Backup DSi NAND` y luego presiona (A).
  - Esto tomará unos minutos
  - Guarda esta copia de la NAND en una ubicación segura, es una copia crítica y la necesitaremos después para instalar HiyaCFW.
  - Cuando aparezca `saved nand.bin.sha1.` la copia se habrá terminado de crear.
6. Navega a `Exit` y presiona (A).

## Instalación

1. Navega a `unlaunch.nds` y luego presiona (A).
  - El instalador de Unlaunch debería aparecer.
2. Navega a `INSTALL NOW` y presiona (A).
  - Si el instalador de Unlaunch se congela en `ERROR: MISMATCH IN FAT COPIES` por favor lee el [FAQ](/ayuda/faq).
3. Cuando acabe, navega a `POWER DOWN` y presiona (A).
  - Tu consola se apagará.
4. Enciende tu consola de nuevo.
  - La pantalla de gestión de Unlaunch debería aparecer.
5. Apaga tu consola.


Con Unlaunch instalado tu consola tiene un sistema antibrick muy primitivo, a menos que el archivo TMD sea destruido. Unlaunch tiene protecciones para prevenir que esto pase, y HiyaCFW usa tu tarjeta SD como la NAND de tu consola, añadiendo una fuerte capa de protección antibrick.

[Instalando HiyaCFW](/guia_dsi/guía/instalando-hiyacfw){: .btn .btn--light-outline}
{: style="text-align: center;"}
