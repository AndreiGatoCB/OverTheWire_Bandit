# BANDIT 8

### Los comandos que ejecuté para resolver este nivel fueron los siguientes

- **_Comando de conexión:_** `ssh bandit8@bandit.labs.overthewire.org -p 2220`

- **_Contraseña:_** `_______`

- **_Listar archivos y directorios en el directorio:_** `ls`

- **_Buscar una línea que se repite sólo una vez en el archivo
  :_** `sort data.txt | uniq -u`
    - sort: organizar las líneas del archivo.
    - |: asigna el elemento de la izquierda al filtrado de la derecha dado con uniq.
    - uniq: Filtra el archivo seleccionando las líneas que se repiten una sola vez en el archivo.
      > -c: cuenta repeticiones de cada línea.
      
      > -d:	Muestra líneas duplicadas.
      
      > -u:	Muestra líneas únicas.
      
      > -i:	Ignora mayúsculas/minúsculas al comparar.

      > -f N:	Ignora los primeros N campos (separados por espacios/tabs) al comparar.
      
      > -s N:	Ignora los primeros N caracteres al comparar.
      
      > -w N:	Compara solo los primeros N caracteres de cada línea.


Con estos comandos tendremos acceso a la contraseña para acceder al nivel 9 de OTW.

Las contraseñas se encontrarán realizando el nivel en [OTW8][1]

[1]: https://overthewire.org/wargames/bandit/bandit9.html
