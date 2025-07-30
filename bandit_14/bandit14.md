 BANDIT 14

### Los comandos que ejecuté para resolver este nivel fueron los siguientes

- **_Comando de conexión:_** `ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220`

- **_Contraseña:_** `_______`

- **_Abrir la contraseña de bandit 14:_** `cat /etc/bandit_pass/bandit14`
  > En otro nivel habíamos visto que la contraseña de cada nivel se encuentra en `/etc/bandit_pass/banditXX`
  > A este archivo sólo puede accederse desde el nivel 14, por los permisos de uso.
  
- **_Escribir datos a traves de la conexión de red
  :_** `nc localhost 30000`
  > Puede ser usada para conexiones TCP y UDC.
  > nc es por NetCat
  > La sintaxis es `nc <host> <puerto>`

- **_Introducir la contraseña del nivel 14
  :_** `_______`

Con estos comandos tendremos acceso a la contraseña para acceder al nivel 15 de OTW.

Las contraseñas se encontrarán realizando el nivel en [OTW14][1]

[1]: https://overthewire.org/wargames/bandit/bandit15.html
