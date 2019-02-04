---
title: Comprobación de SD
layout: single
sidebar:
  nav: "side"
---

Puede que este anexo necesite actualización.
{: .notice--info}

Esta es una sección adicional para revisar tu tarjeta SD en busca de errores. Dependiendo del tamaño tu tarjeta SD y la velocidad de tu computadora, ¡este proceso podría tardar varias horas!

Sigue las instrucciones en base a tu sistema operativo:

## Windows
### Descargas
- La última versión de [h2testw](http://www.heise.de/ct/Redaktion/bo/downloads/h2testw_1.4.zip)

### Instrucciones
1. Copia `h2testw.exe` del archivo `.zip` de h2testw al escritorio.
2. Inserta tu tarjeta SD en tu computadora.
3. Ejecuta `h2testw.exe`.
4. Selecciona "English".
5. Selecciona "Select target".
6. Selecciona la letra de la unidad de tu tarjeta SD.
7. Asegúrate de que "all available space" esté seleccionado.
8. Haz clic en "Write + Verify".
9. Espera hasta que se complete el proceso.

Si se muestra el resultado `Test finished without errors`, significa que tu tarjeta SD está en buen estado y puedes borrar todos los archivos `.h2w` de tu tarjeta SD.
{: .notice--success}

Si la comprobación muestra otro tipo de resultado, ¡tu tarjeta SD puede estar corrupta o dañada y tendrás que reemplazarla!
{: .notice--danger}

## macOS
### Descargas
- La última versión de [F3X](https://github.com/insidegui/F3X/releases/latest)

### Instrucciones
1. Descomprime el archivo `.zip` de F3X.
2. Inserta tu tarjeta SD en la computadora.
3. Ejecuta la aplicación F3X.
4. Selecciona tu tarjeta SD.
5. Haz clic en "Start Test".
6. Espera hasta que se complete el proceso.

Si la comprobación muestra el resultado `Success! Your card is ok!` tu tarjeta SD está bien y puedes borrar todos los archivos `.h2w` de tu tarjeta SD.
{: .notice--success}

Si la comprobación muestra otro tipo de resultado, ¡tu tarjeta SD puede estar corrupta o dañada y tendrás que reemplazarla!
{: .notice--danger}

## Linux
### Descargas
- La última versión de [F3](https://github.com/AltraMayor/f3/releases/latest)

### Instrucciones
1. Descomprime el archivo `.zip` de f3.
2. Haz `cd` al directorio de f3.
3. Ejecuta `make` para compilar F3.
4. Inserta tu tarjeta SD en tu computadora.
5. Monta tu tarjeta SD.
6. Ejecuta `./f3write <el punto de montaje de tu tarjeta sd>`.
7. Espera hasta que se complete el proceso. Revisa un ejemplo de salida a continuación.

~~~ bash
$ ./f3write /media/michel/6135-3363/
Free space: 29.71 GB
Creating file 1.h2w ... OK!
...
Creating file 30.h2w ... OK!
Free space: 0.00 Byte
Average Writing speed: 4.90 MB/s
~~~

8. Ejecuta `./f3read <el punto de montaje de tu tarjeta sd>`.
9. Espera hasta que se complete el proceso. Revisa un ejemplo de salida a continuación.

~~~ bash
$ ./f3read /media/michel/6135-3363/
									SECTORS      ok/corrupted/changed/overwritten
Validating file 1.h2w ... 2097152/        0/      0/      0
...
Validating file 30.h2w ... 1491904/        0/      0/      0

	Data OK: 29.71 GB (62309312 sectors)
Data LOST: 0.00 Byte (0 sectors)
					Corrupted: 0.00 Byte (0 sectors)
	Slightly changed: 0.00 Byte (0 sectors)
				Overwritten: 0.00 Byte (0 sectors)
Average Reading speed: 9.42 MB/s
~~~

Si la comprobación muestra el resultado `Data LOST: 0.00 Byte (0 sectors)` tu tarjeta SD está bien y puedes borrar todos los archivos `.h2w` de tu tarjeta SD.
{: .notice--success}

Si la comprobación muestra otro tipo de resultado, ¡tu tarjeta SD puede estar corrupta o dañada y tendrás que reemplazarla!
{: .notice--danger}

[Comencemos](/guia_dsi/guía/comencemos){: .btn .btn--light-outline}
{: style="text-align: center;"}
