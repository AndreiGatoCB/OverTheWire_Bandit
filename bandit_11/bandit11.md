# BANDIT 11

### Los comandos que ejecuté para resolver este nivel fueron los siguientes

- **_Comando de conexión:_** `ssh bandit11@bandit.labs.overthewire.org -p 2220`

- **_Contraseña:_** `_______`

- **_Listar archivos y directorios en el directorio:_** `ls`

- **_Descifrar un archivo cuyos caracteres están rotados 13 lugares.
  :_** `cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'`
    - cat: es el comando que se utiliza para abrir un archivo.
    - |: separa el comando que abre el archivo del comando tr.
    - tr: permite reemplazar caracteres con otros. Su sintaxis es: ``tr 'antiguos caracteres' 'nuevos caracteres'.``
      > tr viene de `translate`

Con estos comandos tendremos acceso a la contraseña para acceder al nivel 12 de OTW.

Las contraseñas se encontrarán realizando el nivel en [OTW11][1]

[1]: https://overthewire.org/wargames/bandit/bandit12.html
