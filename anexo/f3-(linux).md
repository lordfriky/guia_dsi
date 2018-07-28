---
title: F3 (Linux)
layout: single
sidebar:
  nav: "side"
---

Puede que esta parte necesite actualización.
{: .notice--info}

Esta es una sección adicional para revisar tu tarjeta SD en busca de errores usando F3.

Dependiendo del tamaño de tu tarjeta SD y la velocidad de tu computadora, ¡este proceso podría tardar varias horas!

Esta página es sólo para usuarios de Linux. Si no estás en Linux, revisa las páginas [H2testw (Windows)](/anexo/h2testw-(windows)) o [F3X (macOS)](/anexo/f3x-(macos)).

## Descargas

- La última versión de [F3](https://github.com/AltraMayor/f3/releases/latest)

## Instrucciones

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

___

Si la comprobación muestra el resultado `Data LOST: 0.00 Byte (0 sectors)` tu tarjeta SD está bien y puedes borrar todos los archivos `.h2w` de tu tarjeta SD.
{: .notice--success}

Si la comprobación muestra otro tipo de resultado, ¡tu tarjeta SD puede estar corrupta o dañada y tendrás que reemplazarla!
{: .notice--danger}

[Comencemos](/guía/comencemos){: .btn .btn--light-outline}
{: style="text-align: center;"}
