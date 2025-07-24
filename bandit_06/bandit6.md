# BANDIT 6

### Los comandos que ejecuté para resolver este nivel fueron los siguientes

- **_Comando de conexión:_** `ssh bandit6@bandit.labs.overthewire.org -p 2220`

- **_Contraseña:_** `_______`

- **_Listar archivos y directorios en el directorio:_** `ls`
  > En este caso no nos mostrará nada.

- **_Buscar un archivo por su usuario propietario, su grupo propietario y su tamaño específico
    :_** `find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null`
    - find: Es el comando para buscar.
    - /: Se usa para realizar la búsqueda en el directorio raiz, ya que en el directorio en el
      que nos encontramos no hay archivos (excepto por los archivos secretos).
    - -tipe: Se usa para definir el tipo de elemento que buscamos.
      > f: Archivos, d: directorios
    - -user: Filtra por el usuario al que pertenece el elemento buscado.
    - -group: Filtra por el grupo al que pertenece el elemento que estamos buscando.
    - -size: Filtra por el tamaño del elemento.
      > c: Bytes, k: Kilobytes, M: Megabytes, G: Gigabytes, empty: 512 bytes
    - 2>/dev/null: Elimina del resultado todos aquellos resultados que presenten un error.
  
- **Abrir el archivo sin entrar en el directorio:** `cat /var/lib/dpkg/info/_______._______`

Con estos comandos tendremos acceso a la contraseña para acceder al nivel 7 de OTW.

Las contraseñas se encontrarán realizando el nivel en [OTW6][1]

[1]: https://overthewire.org/wargames/bandit/bandit7.html
