# BANDIT 11

### Los comandos que ejecuté para resolver este nivel fueron los siguientes

- **_Comando de conexión:_** `ssh bandit11@bandit.labs.overthewire.org -p 2220`

- **_Contraseña:_** `_______`

- **_Listar archivos y directorios en el directorio:_** `ls`

- **_Crear un directorio temporal para no ocupar el directorio del servidor
  :_** `mktemp -d`
    - mktemp: Es el comando para crear elementos temporales.
      > -d: directorios

- **_Copiar el archivo data.txt en la carpeta temporal
  :_** `cp data.txt /tmp/tmp.xovoFXzqhK`

- **_Acceder a la carpeta temporal
  :_** `cd /tmp/tmp.xovoFXzqhK`

- **_Acceder a la carpeta temporal
  :_** `cd /tmp/tmp.xovoFXzqhK`

- **_Renombrar el archivo a hexdump_data sin el sufijo txt
  :_** `mv data.txt hexdumpdata`

- **_Revisar las primeras líneas del archivo para encontrar el tipo de compresión
  en los primeros 6 caracteres
  :_** `cat hexdump_data | head`
  > _Acá busqué el tipo de compresión en la página de wikipedia[^1] y era gzip_

- **_Revertir el hexdump para tener la data original
  :_** `xxd -r hexdump_data2 compressed_data`

- **_Renombrar el archivo compressed_data agregando el sufijo .gz
  :_** `mv compressed_data compressed_data.gz`

- **_Descomprimir el archivo compressed_data.gz
  :_** `gzip -d compressed_data.gz`
  > -d: Descomprimir  

- **_Revisar las primeras líneas del archivo para encontrar el tipo de compresión
  en los primeros 6 caracteres
  :_** `xxd compressed_data | head`
  > _Acá busqué el tipo de compresión en la página de wikipedia[^1] y era bzip2_

- **_Agregar el sufijo bz2
  :_** `mv compressed_data compressed_data.bz2`

- **_Revisar las primeras líneas del archivo para encontrar el tipo de compresión
  en los primeros 6 caracteres
  :_** `xxd compressed_data | head`
  > _En este caso hay un archivo llamado data5.bin_

- **Agregar el sufijo .tar para poder extraer el archivo
  :_** `mv compressed_data compressed_data.tar`

- **_Extraer el archivo al interior de `compressed_data.tar`
  :_** `tar -xf compressed_data.tar`

- **_Revisar las primeras líneas del archivo para encontrar el tipo de compresión
  en los primeros 6 caracteres
  :_** `xxd compressed_data | head`
  > _En este caso hay un archivo llamado data6.bin_

- **_Extraer el archivo al interior de `data5.bin`
  :_** `tar -xf data5.bin`

- **_Revisar las primeras líneas del archivo para encontrar el tipo de compresión
  en los primeros 6 caracteres
  :_** `xxd data6.bin`
  > _Acá busqué el tipo de compresión en la página de wikipedia[^1] y en este caso
  > es un cifrado bzip2_

- **_Cambiar el sufijo del archivo a .bz2
  :_** `mv data6.bin data6.bz2`

- **_Descomprimir el archivo data6.bz2
  :_** `bzip2 -d data6.bz2`

- **_Revisar las primeras líneas del archivo para encontrar el tipo de compresión
  en los primeros 6 caracteres
  :_** `xxd data6.bin`
  > _En este caso hay un archivo llamado data8.bin_

- **_Agregar el sufijo .tar al archivo data6
  :_** `mv data6 data6.tar`

- **_Extraer el archivo al interior de `data6.tar`
  :_** `tar -xf data6.tar`

- **_Revisar las primeras líneas del archivo para encontrar el tipo de compresión
  en los primeros 6 caracteres
  :_** `xxd data8.bin | head`
  > _Acá busqué el tipo de compresión en la página de wikipedia[^1] y en este caso
  > es un cifrado gzip_
  
- **_Cambiar el sufijo .bin al archivo data8.bin por .gz
  :_** `mv data8.bin data8.gz`

- **_Descomprimir el archivo data8.gz
  :_** `gzip -d data8.gz`

- **_Revisar las primeras líneas del archivo para encontrar el tipo de compresión
  en los primeros 6 caracteres
  :_** `xxd data8 | head`
  > _Acá el archivo muestra en el cifrado la respuesta_

- **_Abrimos el archivo data8
  :_** `cat data8`
  
Con estos comandos tendremos acceso a la contraseña para acceder al nivel 12 de OTW.

Las contraseñas se encontrarán realizando el nivel en [OTW11][1]

[1]: https://overthewire.org/wargames/bandit/bandit12.html
[^1]: https://en.wikipedia.org/wiki/List_of_file_signatures
