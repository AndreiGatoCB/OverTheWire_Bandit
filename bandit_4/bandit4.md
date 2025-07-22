 BANDIT 4

### Los comandos que ejecuté para resolver este nivel fueron los siguientes

- **_Comando de conexión:_** `ssh bandit4@bandit.labs.overthewire.org -p 2220`

- **_Contraseña:_** `_______`

- **_Listar archivos y directorios en el directorio:_** `ls`

- **_Entrar en el directorio_ inhere _:_** `cd inhere`

- **_Listar archivos y directorios en el directorio:_** `ls`

**Método 1: Más fácil, menos práctico.**
- **_Leer un archivo que empieza con un guión:_** `cat ./-file00`
  
- **_Repetir hasta que encontremos el archivo que no esté cifrado._**

**Método 2: Más complejo, más práctico.**

- **_Identificar qué tipo de datos contienen todos los archivos de un directorio:_** `file ./*`
  
- **_Abrir el archivo de tipo texto no cifrado como data:_** `cat ./-file0_`

Con estos comandos tendremos acceso a la contraseña para acceder al nivel 5 de OTW.

Las contraseñas se encontrarán realizando el nivel en [OTW4][1]

[1]: https://overthewire.org/wargames/bandit/bandit5.html
