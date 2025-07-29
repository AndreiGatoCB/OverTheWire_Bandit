# BANDIT 13

### Los comandos que ejecuté para resolver este nivel fueron los siguientes

- **_Comando de conexión:_** `ssh bandit13@bandit.labs.overthewire.org -p 2220`

- **_Contraseña:_** `_______`

- **_Listar archivos y directorios en el directorio:_** `ls`
  > La llave privada es `sshkey.private`

- **_Salir del servidor conociendo el nombre de la llave privada
  :_** `exit`

- **_Descargar la llave privada a mi computador
  :_** `scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private .`

- **_Contraseña:_** `_______`
  > Acá va la contraseña del nivel 13
  > Esto descargará la llave privada en el directorio en el que estamos trabajando en la terminal.

- **_Comando de conexión a over the wire con la llave privada en lugar de una contraseña
  :_** `ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220`

Con estos comandos tendremos acceso a la contraseña para acceder al nivel 14 de OTW.

Las contraseñas se encontrarán realizando el nivel en [OTW13][1]

[1]: https://overthewire.org/wargames/bandit/bandit14.html
