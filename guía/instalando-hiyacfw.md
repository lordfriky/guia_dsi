---
title: Instalando HiyaCFW
layout: single
sidebar:
  nav: "side"
---

¡No actualizes el sistema después de crear la SDNAND! Esto removerá los parches de HiyaCFW.
{: .notice--danger}

Tener instalado HiyaCFW tiene severas ventajas que Unlaunch por sí solo no provee, por ejemplo:

- Ejecutar el sistema desde una tarjeta SD (SDNAND).
- Instalar homebrews en el menú del sistema con facilidad.
- Configurar una imagen personalizada al arranque de la consola.
- Arrancar automáticamente en otra aplicación, como TWiLight Menu++.

Además en el proceso se instalará TWiLight Menu++ automáticamente, el cual luego configuraremos para que sustituya al menú de sistema oficial.

## Requisitos

- Una copia de tu NAND.
  - Deberías tener esto de una sección anterior.
- La última versión de [HiyaCFW Helper](https://github.com/mondul/HiyaCFW-Helper/releases/latest){:target="_ blank"}
  - Los usuarios de Windows pueden usar los binarios compilados, mientras que los usuarios de otros sistemas operativos deberán usar el `.py` (requiere [Python 3](https://www.python.org/downloads/){:target="_ blank"}).
  - Los usuarios de Windows deberán tener instalada la versión `V2.0.1001` de [OSFMount](https://www.osforensics.com/downloads/osfmount_x64_v2.0.1001.exe) ([versión de 32 bits](https://www.osforensics.com/downloads/osfmount_v2.0.1001.exe)).

## Instrucciones

1. Inserta tu tarjeta SD en tu ordenador.
2. Copia *el contenido de* el archivo `.zip` de HiyaCFW Helper a alguna carpeta en tu ordenador.
3. Abre HiyaCFW Helper.
  - Los usuarios de Windows tendrán que abrirlo como administrador.
  - Los usuarios de macOS tendrán que abrirlo desde una terminal con `python3 HiyaCFW_Helper.py` dado a que la versión de Python 2 preinstalada con el sistema es usada por defecto.
4. Haz clic en el botón `...`.
5. Busca tu copia de la NAND y haz clic en `Abrir`.
  - Debería estar dentro de tu tarjeta SD dentro de una carpeta de nombre `FW00XXXXXXXXXX`.
6. Presiona `Start`.
  - Asegúrate de dejar marcada la casilla `Install latest TWiLight Menu++ on latest firmware` antes de continuar.
7. Navega hasta la raíz de tu tarjeta SD y presiona `OK`.
  - El proceso tardará algunos minutos.
  - Cuando la ventana de HiyaCFW Helper muestre un mensaje diciendo `Done!`, el proceso se habrá completado.
8. Cierra HiyaCFW Helper.
9. Saca la tarjeta SD de tu ordenador y vuélvela a introducir en tu DSi.

[Finalizar Instalación](/guia_dsi/guía/finalizar-instalación){: .btn .btn--light-outline}
{: style="text-align: center;"}
