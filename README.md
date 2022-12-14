# Git and GitHub course

<img src="https://cliparting.com/wp-content/uploads/2017/09/Superman-clipart-3.jpeg"/>

## Primeros comandos de git

version de git: `git --version`

git help: `git help`

salir de la consola git: `:q`

## Configurar git

- `$ git config --global user.name "Fernando Herrera"`

- `$ git config --global user.email "fernandoherrera@hola.com"`

El correo electronico puede ser un email general que no esta siendo utilizado en github

Para ver los cambios que acabamos de hacer en la configuracion, escribimos:

- `$ git config --global -e`

## Git Fundamentos

**Inicaliza el repositorio (proyecto) git:**

`$ git init`

**Informacion sobre los commits, ramas en las que nos encontramos, etc**

`$ git status`

**Añadir archivos**

`$ git add <nombre del archivo>`

`$git add .` añade todos los archivos

**Eliminar un archivo en particular**

`$ git reset <nombre del archivo>`

**Commit**

`$ git commit -m "<mensaje del commit">`

Cada commit nos permite viajar en el tiempo dentro del repositorio para conocer el punto inicial del repositorio, su estado en una fecha en particular, etc

**Recuperar mi proyecto al codigo en el que estaba anteriormente**

`$ git checkout -- .`

Este comando sirve para recuperar código de un archivo ya sea html, css, js, etc que por algún motivo en particular se perdió. Este comando reconstruye el código dentro del archivo y también recupera directorios que se borraron, ejemplo: `src - scss - js- etc`

**Conocer el branch en el que nos encontramos**

`$ git branch`

Un branch es el lugar en el que estamos trabajando con el repositorio (proyecto)

<img src="https://wac-cdn.atlassian.com/dam/jcr:a905ddfd-973a-452a-a4ae-f1dd65430027/01%20Git%20branch.svg?cdnVersion=471"/>

Siempre es recomendable trabajar con diversos branchs

**Ver logs del repositorio**

`$ git log`

Para ver un "resumen de los logs" hacemos

`$ git log --oneline`

**Comodines en git**

Si quiero enviar al stage todos los archivos con extensión `html` podemos realizar el sgte comando:

`$ git add *.html`

Si queremos agregar archivos por ejemplo `js` que estén desde el root y que esten guardados en una carpeta en particular, realizamos el sgte comando:

`$ git add js/*.js`

Esto toma todos los archivos con la extension `*.js` que están dentro de la carpeta `js/`

Para agregar todos los archivos que se encuentran en la carpeta `css` por ejemplo, realizamos el sgte comando:

`$ git add css/`

Este comando añade al stage todos los archivos que están dentro de la carpeta 'css'

**Ver el status de los archivos en git de forma resumida**

`$ git status --short`

**Crear un alias en git**

`$ git config --global alias.s "status --short"`

Este comando crea el alias `s` con el que se podrá ver el status de los archivos de forma resumida

Para ver la configuracion global hacemos

`$ git --global e`
