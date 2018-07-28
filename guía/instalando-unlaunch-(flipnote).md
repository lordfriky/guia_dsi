---
title: Instalando Unlaunch (Flipnote)
layout: single
sidebar:
  nav: "side"
---
Antes de proceder, si la región de tu consola es USA, asegúrate de que el idioma de tu consola esté establecido en inglés.
{: .notice--info}

Unlaunch actualmente está en beta. Por favor, procede con precaución.
{: .notice--info}

Unlaunch es un explit de inicio de DSi que te permitirá instalar HiyaCFW, un custom firmware para DSi, en tu consola. Debido a un bug en el instalador de la versión 0.9, instalaremos Unlaunch v0.8 y lo usaremos para actualizar a la última versión.

## Descargas

- [Unlaunch v0.8](https://problemkaputt.de/unlau08.zip)
- La última versión de [Unlaunch](https://problemkaputt.de/unlaunch.zip)
- La última versión de [HBMenu](https://github.com/devkitPro/nds-hb-menu/releases/){:target="_ blank"}
- La última versión de [ugopwn](/guia_dsi/archivos/ugopwn.zip)
- La última versión de [fwTool](/guia_dsi/archivos/fwTool.nds)

## Preparando la tarjeta SD

1. Inserta tu tarjeta SD en tu ordenador.
2. Copia el contenido del archivo `.zip` de ugopwn a la raíz de tu SD.
3. Copia el archivo `.nds` de fwTool a la raíz de tu tarjeta SD.
4. Copia `BOOT.NDS` de la carpeta `hbmenu` del archivo `.tar.bz2` de HBMenu a la raíz de tu tarjeta SD.
5. Saca la tarjeta SD de tu ordenador y vuélvela a introducir en tu DSi.

## Creando una copia de la NAND

1. Abre la aplicación de Flipnote Studio.
  - Asegúrate de que *Calendario al inicio* esté desactivado en los ajustes de Flipnote Studio.
  - Si ya tienes otro exploit de DSiWare instalado avanza directamente hasta el paso 14.
  - Toma en cuenta que Sudokuhax *no puede* hacer una copia adecuada de la NAND con el footer requerido
2. Elige **Ver nota > Tarjeta SD > Seleccionar carpeta > Usuario > ugopwn**.
3. Haz clic en el flipnote con la mitad inferior roja.
4. Elige "Modificar".
5. Haz clic en el icono de la rana de Flipnote de la esquina inferior izquierda.
6. Haz clic en el icono de rollo de película.
7. Elige **Copiar > Atrás > Salir**.
8. Haz clic en la segunda nota y elige "Modificar".
9. Haz clic en el icono de la rana de Flipnote de la esquina inferior izquierda.
10. Haz clic en el icono de rollo de película.
11. **Región USA/EUR/AUS:** Pulsa el botón derecho del d-pad 2 veces.
  - Debería de haberse creado un nuevo frame.
12. Basado en tu región, haz lo siguiente:
  - **Región USA:** Haz click en el botón pegar exactamente 122 veces.
  - **Región EUR/AUS:** Haz click en el botón pegar exactamente 2 veces.
  - **JPN:** Haz clic en el botón pegar.
13. **Región USA/EUR/AUS:** Selecciona "Borrar" y después "Pegar".
  - Esto debería lanzar HBMenu.
14. Navega a `fwtool.nds` y luego presiona (A).
  - fwTool debería aparecer.
15. Navega a `Backup DSi NAND` y luego presiona (A).
  - Esto tomará unos minutos
  - Guarda esta copia de la NAND en una ubicación segura, es una copia crítica y la necesitarémos despues para instalar HiyaCFW.
  - Cuando aparezca `saved nand.bin.sha1.` la copia se habrá terminado de crear.
16. Navega a `Exit`, presiona (A) y apaga tu consola.

## Instalación

1. Inserta tu tarjeta SD en tu ordenador.
2. Copia `UNLAUNCH.DSI` del archivo `.zip` de **Unlaunch v0.8** a la raíz de tu tarjeta SD.
3. Renombra `UNLAUNCH.DSI` a `unlaunch.nds`.
4. Copia `UNLAUNCH.DSI` del archivo `.zip` de **_la última versión_ de Unlaunch** a la raíz de tu tarjeta SD.
5. Renombra `UNLAUNCH.DSI` a `bootcode.dsi`.
6. Saca la tarjeta SD de tu ordenador y vuélvela a introducir en tu DSi.
7. Enciende tu consola, y repite los pasos 1 a 13 de **Creando una copia de la NAND**.
  - Esto debería lanzar HBMenu.
8. Navega a `unlaunch.nds` y luego presiona (A).
  - El instalador de Unlaunch aparecerá.
9. Navega a `INSTALL NOW` y presiona (A).
  - Si Unlaunch se congela en `ERROR: MISMATCH IN FAT COPIES` por favor lee nuestro [FAQ](/guia_dsi/help/faq).
10. Cuando acabe, navega a `POWER DOWN` y presiona (A).
  - Tu consola se apagará.
11. Enciende tu consola de nuevo.
  - El instalador de Unlaunch aparecerá de nuevo, este es el de la última versión.
12. Repite los pasos 9 y 10 de esta sección.
13. Presiona (A) mientras enciendes tu consola, para verificar que Unlaunch se haya instalado correctamente.
  - Deberás ver brevemente la pantalla de Unlaunch, y luego arrancar en una versión del menú de DSi sin sonido.
  - Si estás en un firmware superior a 1.4, es **muy probable** que tu consola se congele en el menú de Unlaunch, debido a un bug en Unlaunch 0.9
  - Puedes regresar a 0.8 ejecutando su instalador como `bootcode.dsi`, pero perderás la habilidad de ejecutar DSiWare fácilmente con DSiMenu++

Con Unlaunch instalado tu consola tiene un sistema antibrick muy primitivo, a menos que el archivo TMD sea destruido. Unlaunch tiene protecciones para prevenir que esto pase, y HiyaCFW usa tu tarjeta SD como la NAND de tu consola, añadiendo una fuerte capa de protección antibrick.

Ahora puedes eliminar el archivo `bootcode.dsi` de tu tarjeta SD. Esto hará que no tengas que presionar (A) mientras enciendes la consola.

[Instalando HiyaCFW](/guia_dsi/guía/instalando-hiyacfw){: .btn .btn--light-outline}
{: style="text-align: center;"}
