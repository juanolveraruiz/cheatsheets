# Git Cheatsheets

Git es como una memoria para código, te ayuda a guardar tu progreso en tu compuradora o remoto si es que usas github.

## Lo básico

### git init

Este comando se usa para iniciar un repositorio de git en el directorio actual. Es como meter una tarjeta de memoria en un videojuego para guardar tu progreso.

### git add

Con esto seleccionas que es lo que quieres guardar, por ejemplo, si tienes muchos archivos y solo quieres guardar el archivo "script.js" el comando que usarias sería:

    git add script.js

Si quieres agregar varios solo usa espacios, por ejemplo si quisiera guardar también el archivo "index.html" el comando sería:

    git add script.js index.html

Si tienes muchos archivos que añadir puedes usar un <kbd>.</kbd> para agregarlos todos, por ejemplo:

    git add .

### git commit

Este comando se usa para guardar los archivos que ya pusiste en el "staging area" al usar git add. en estos ejemplos serían los archivos index.html y script.js. lo normal es que comando se use con un "-m" que indica que agregaremos un mensaje a este commit, eso nos ayudará adescribir los cambios que se estan guardando. por ejemplo:

    git commit -m "se agregaron los archivos index.html y script.js, en el index se añadieron enlaces a otras páginas y en el script se añadio un array con claves para las devoluciones"

### git log

Si ya has hecho varios cambios en tu código y has estado guardando tu proceso con `commit`, puedes ver un listado de las veces que has guardado cambios en tu código con el comando `git log`. El resultado de usar este comando se vería algo así:

    commit f5a66d78704f3a087d6122a46ec48898afabe653d
    Author: Juan Olvera <juan@gmail.com>
    Date: Sat Oct 11 22:53:54 -0600

        aquí debería aparecer el mensaje con el cual hiciste este commit

El todo lo que se ve después del `commit` es un hashcode, que te puede servir para volver a ese punto en el tiempo de tu código si es que cometes errores o te arrepientes de ciertos cambios.

### git checkout

Aquí esto es simple, es más como una pequeña extención del `git log` ya que si quieres corregir algo o volver a una versión pasada de tu código necesitas primero usar `git log` para obtener el hashcode del punto al que quieres volver. Leer los mensajes en tus commits podría ser de ayuda para identificar cual hashcode vas a usar. Cuando sepas cual necesitas solo tienes que copiarlo y para volver a ese punto en tu código usas el comando `git checkout`, ejemplo:

    git checkout f5a66d78704f3a087d6122a46ec48898afabe653d

## Trabajo remoto

### GitHub

Una de las mejores maneras que hay para trabajar remoto y contribuir con el código de los demás es GitHub. Sé que hay varias opciones que son como lo mismo o similar a GitHub como BitBucket, GitLab y demás, pero GitHub es la más popular así que en GitHub encontramos la mayor cantidad de repositorios. Incluso grandes empresas como Microsoft, Meta y Apple lo usan.

#### ¿Cómo subo un repositorio a GitHub?

Para este punto debemos de suponer que tu ya tienes un perfil o cuenta de GitHub. En tu perfil debes encontrarte un apartado de "Repositories", al entrar debe haber un botón para crear uno nuevo que diga <kbd>New</kbd>. Al presionarlo te pedira que le pongas un nombre, le añadas una descripción (opcional), selecciones si es un repositorio privado o público y también te dará la opción de iniciar ese repositorio con archivos `README.md`, un `.gitignore` y escoger una licencia. Luego tenemos dos opciones, podemos crear un nuevo repositorio local y conectarlo con el remoto que acabamos de hacer en GitHub o mandar a GitHub uno que ya teníamos en nuestra máquina.
