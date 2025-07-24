# BANDIT 5

### Los comandos que ejecuté para resolver este nivel fueron los siguientes

- **_Comando de conexión:_** `ssh bandit5@bandit.labs.overthewire.org -p 2220`

- **_Contraseña:_** `_______`

- **_Listar archivos y directorios en el directorio:_** `ls`

- **_Entrar en el directorio_ inhere _:_** `cd inhere`

- **Método 1:**
  - **_Listar todos los archivos y directorios incluídos los secretos 
  en el directorio:_** `ls -la` 

  - **_Listar todos los archivos de un directorio sin necesidar de 
  entrar al directorio:_** `ls -la maybehere00` 

  - **_Listar todos los archivos de todos los directorios del directorio
  principal:_** `file */*`
  
  - **_Listar todos los archivos, incluídos los archivos secretos,
  de todos los directorios del directorio principal:_** `file */{.,}*` 

  - **_Filtrar todos los archivos de texto legible:_** `file */{.,}* | grep ASCII`
  
  - **_Filtrar por el tamaño del archivo en el directorio principal
    :_** `du -b -a | grep 1033`
    - du: filtrar por tamaño.
    - -b: especificar que es en bytes.
    - -a: analizar todos los archivos, incluídos los secretos.
    - |: Separar una parte de la consulta de otra
    - grep: busca el input que se da a la izquierda del pipe con las
      indicaciones del grep.
  
  - **Abrir el archivo sin entrar en el directorio:** `cat ./maybehere__/.file_`

- **Método 2:**
  - **_Buscar un elemento entre todos los directorios del directorio principal
    :_** `find .`
    
  - **_Buscar elementos de tipo archivo:_** `- type f`
  
  - **_Buscar por el tamaño del archivo:_** `size 1033c`
  
  - **_NO tener en cuenta archivos ejecutables:_** `! -executable`
  
  - **_Ejecutar el comando file con estas instrucciones:_** `-exec file '{}' \;`
  
  - **_Filtrar por tipo de archivo ASCII (Legible por humanos):_** `| grep ASCII`
 
  - **_Todo el comando junto se debe ver así:_** `find . -type f -size 1033c !
    -executable -exec file '{}' \; | grep ASCII`

   - **Abrir el archivo sin entrar en el directorio:** `cat ./maybehere__/.file_`

Con estos comandos tendremos acceso a la contraseña para acceder al nivel 6 de OTW.

Las contraseñas se encontrarán realizando el nivel en [OTW5][1]

[1]: https://overthewire.org/wargames/bandit/bandit6.html
