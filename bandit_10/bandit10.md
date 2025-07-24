# BANDIT 10

### Los comandos que ejecuté para resolver este nivel fueron los siguientes

- **_Comando de conexión:_** `ssh bandit10@bandit.labs.overthewire.org -p 2220`

- **_Contraseña:_** `_______`

- **_Listar archivos y directorios en el directorio:_** `ls`

- **_Buscar una línea específica en un archivo basada en una cadena de texto dada
  :_** `base64 data.txt -d`
    - base64: es el comando de linux que se encarga del cifrado y descifrado de archivos en base64.
    - -d: la bandera de base64 para descifrar.

Con estos comandos tendremos acceso a la contraseña para acceder al nivel 11 de OTW.

Las contraseñas se encontrarán realizando el nivel en [OTW10][1]

[1]: https://overthewire.org/wargames/bandit/bandit11.html
