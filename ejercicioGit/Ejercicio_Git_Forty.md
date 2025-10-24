# 01 - Ejercicio de Git - Forty - local y remoto

[TOC]

## Trabajo en local

> Este trabajo se ha realizado en Windows y en Mac. Para evitar confusiones se ha  renombrado el proyecto a `forty2` en Mac para que se vieran todos lo flujos de trabajo en local en mi dispositivo .



> Antes de nada, abrimos la terminal y nos colocamos en la carpeta donde queremos inicializar el repositorio o si estamos en Windows directamente desde la carpeta damos al boton derecho y escogemos la terminal bash.

1. Inicializar un nuevo repositorio Git en una carpeta llamada `"forty"` y agrega los archivos proporcionados en el aula virtual.

   ```bash
   $ git init
   ```

   Aqui se crea una carpeta `.git` que es lo que nos indica que es un repositorio

   Como no quiero añadir todos los archivos porque algunos los vamos a ignorar, los voy metiendo uno a uno. 

   Listamos para ver que archivos contiene la carpeta:

   ```bash
   $ ls
   ```

   Vamos agregando los archivos que no vamos a ignorar:

   ```bash
   $ git add assets
   ```

   Comprobamos que estan en el staging: (nos dice los que estan trackeados y los que no):

   ```bash
   $ git status
   ```

   Hacemos commit de los que hemos agregado:

   ```bash
   $ git commit -m "Añadidos los archivos iniciales"
   ```

   

2. Renombra la rama master a `main`.

   Este paso no se hace porque en la configuración de Git ya lo hemos hecho.

3. Haz que los ficheros `README.txt`, `LICENSE.txt` y `passwords.txt` sean ignorados por el control de versiones.

    Creamos el `.gitignore` 

   ```bash
   $ touch .gitignore
   ```

   Después abrimos el archivo generado e incluimos el nombre de los archivos que tenemos que ignorar. (editamos el archivo directamente). Aqui ya dejamos escrito el nombre del fichero `passwords.txt` para que lo ignore cuando lo creemos.

   Después debemos añadir este archivo al repositorio .git

   ```bash
   $ git add .gitignore
   ```

   Se hace un commit de este añadido.

   ```bash
   $ git commit -m "Añadido .gitignore para ignorar los archivos sensibles"
   ```

   

4. Crea el archivo `password.txt` . Comprueba que el control de versiones lo ignora.

   Para introducir los ficheros que queremos ignorar los escribimos en el archivo de `.gitignore`. si necesitamos crear alguno como en esta caso el `password.txt` lo hacemos con el comando:  (Se puede usar este o nano)

   ```bash
   $ notepad password.txt
   ```

   Escribimos en él lo que queramos y lo guardamos.

   Para saber que archivos están ignorados lo haremos con una de estas dos formas:

   ```bash
   $ git ls-files --others -i --exclude-standard
   ```

   ```bash
   $ git status
   ```

   

5. Crea una rama llamada `"feature-content"` . Muevete a esa rama. Cambia, en la línea 3477, el `font-size` por `1.5em` en el archivo `main.css` . Ver los logs de la forma más gráfica posible.

   ```bash
   $ git branch feature-content
   ```

   Comprobar que ramas tenemos:

   ```bash
   $ git branch
   ```

   Para cambiarnos de rama:

   ```bash
   $ git checkout feature-content
   ```

   Hacemos los cambios en el fichero  que nos inican y guardamos.

   Para ver los logs de la manera más gráfica:

   ```bash
   $ git log --graph --oneline --all --decorate
   ```

   <img src="./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/image-20251016171335942.png" alt="image-20251016171335942" style="zoom:67%;" />

   Tenemos que añadir los cambios que hemos hecho.

   ```bash
   $ git add assets/css/main.css
   ```

   ```bash
   $ git commit -m "Añadidos cambios en linea 3477, font-size: 1.5em"
   ```

   <img src="./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/image-20251016172207154.png" alt="image-20251016172207154" style="zoom:67%;" />

   Verificamos si hay cambios pendientes:

   ```bash
   $ git status
   ```

   

6. Elimina el archivo `"passwords.txt"` en la carpeta `forty` . Verifica el estado del repositorio. ¿Hay cambios pendientes?

   Voy a la carpeta de `forty` directamente y borro el archivo. Ahora compruebo que ha pasado con el comando:

   ```bash
   $ git status
   ```

   

7. Crea un nuevo archivo llamado `"about.html"` , partiendo del archivo `generic.html` y agrégalo al repositorio, haz un nuevo commit.

   Podemos crearlo directamente en la carpeta o desde comandos:

   Copiamos el estilo y contenido de genreric.html en about.html

   ```bash
   $ cp generic.html about.html
   ```

   Hacemos un cambio en el título y lo renombramos con `About`. Esto lo hacemos desde nano

   ```bash
   $ nano about.html
   ```

   Agregamos este nuevo archivo al repositorio:

   ```bash
   $ git add about.html
   $ git commt -m "Añadida nueva pagina about.html"
   ```

   

8. Cambia a la rama `main`. Examina los logs del repositorio de forma gráfica.

   ```bash
   $ git checkout main
   $ git log --graph --oneline --all --decorate
   ```

   ![Captura de pantalla 2025-10-17 a las 9.27.04](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/Captura%20de%20pantalla%202025-10-17%20a%20las%209.27.04.png)

   

9. Modifica algo en el archivo `generic.html`, comprueba que hay cambios, y realiza otro commit . Examina los logs del repositorio de forma gráfica.

   Abrimos nano para realizar cambios en `generic.html` :

   ```bash
   $ nano generic.html
   ```

   Anadimos los cambios y realizamos commit al repositorio:

   ```bash
   $ git add generic.html
   $ git commit -m "Añadidos cambios en generic.html"
   $ git log --graph --oneline --all --decorate
   ```

   <img src="./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/Captura%20de%20pantalla%202025-10-17%20a%20las%209.36.19.png" alt="Captura de pantalla 2025-10-17 a las 9.36.19"  />

   

10. Modifica algo en el fichero `elements.html`. Confirma los cambios, pero no hagas commit. 

    Abrimos nano para realizar cambios en `elements.html` :

    ```bash
    $ nano elements.html
    ```

    Añadimos los cambios pero no los commiteamos:

    ```bash
    $ git add elements.html
    ```

    Comprobamos que los cambios estan pendientes de confirmación:

    ```bash
    $ git status
    ```

    ![Captura de pantalla 2025-10-17 a las 9.43.30](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/Captura%20de%20pantalla%202025-10-17%20a%20las%209.43.30.png)

    

11. Mira las diferencias de `elements.html`. Los cambios no nos gustan, deshaz los cambios de `elements.html.` Comprueba que no hay cambios pendientes.

    Para deshacer los cambios en staging  primero debemos deshacer el "git add"

    ```bash
    $ git restore --staged elements.html
    ```

    Después deshacer la modificacion que hemos hecho del archivo:

    ```bash
    $ git restore elements.html
    ```

    Por último comprobamos que todo está correcto:

    ```bash
    $ git status
    ```

    > La forma anterior es la mas moderna pero también hay otra que siempre se ha hecho que es:
    >
    > ```bash
    > $ git reset HARD elements.html
    > $ git checkout --elements.html
    > ```
    >
    > 

    ![Captura de pantalla 2025-10-17 a las 9.58.04](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/Captura%20de%20pantalla%202025-10-17%20a%20las%209.58.04.png)

    

12. Muestra las diferencias entre dos ramas. 

    ```bash
    $ git diff main feature-content
    ```

    Muestra los cambios que estan en feature-content que no estan en main. En nuestro caso los cambios qu se hicieron en el archivo `about.html`, en `main.css` y en `generic.html`

    Para que no se vea tanta información de los archivos cambiados se puede cambiar el comando para que solo te muestre el nombre los archivos cambiados: (Cualquiera de las dos nos da una inforamcion más resumida)

    ```bash
    $ git diff main feature-content --name-only
    ```

    

    ```bash
    $ git diff main feature-content --stat
    ```

    ![Captura de pantalla 2025-10-17 a las 10.17.12](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/Captura%20de%20pantalla%202025-10-17%20a%20las%2010.17.12.png)

    

13. Fusiona la rama `"feature-content"` con la rama principal (main). Muestra los logs del repositorio de una forma gráfica y completa.

    Primero nos aseguramso de estar en la rama main:

    ```bash
    $ git checkout main
    ```

    Fusionamos la rama feature-content:

    ```bash
    $ git merge feature-content
    ```

    Mostrar los logs completos:

    ```bash
    $ git log --all --decorate --graph
    ```

    <img src="./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/Captura%20de%20pantalla%202025-10-17%20a%20las%2010.40.19.png" alt="Captura de pantalla 2025-10-17 a las 10.40.19" style="zoom:67%;" />

    <img src="./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/Captura%20de%20pantalla%202025-10-17%20a%20las%2010.39.50.png" alt="Captura de pantalla 2025-10-17 a las 10.39.50" style="zoom: 67%;" />

    

    > Cuando hacemos el merge en Mac nos sale una pantalla de vim para que pongamos un mensaje al merge que queremos realizar. Por lo general ya te pone un mensaje predeterminado.
    >
    > Para aceptar ese mensaje tenemos que realizar unos pasos y asi poder salir de la pantalla:
    >
    > - Presionamos ESC
    > - Escribimos  `:wq`
    > - Presionamos Enter

    Este merge no da errores porque se han hecho cambios diferentes en cada rama pero no coinciden que se hallan hecho cambios en ambas ramas en el mismo archivo en el mismo sitio.

    

14. Crea una nueva rama llamada `" hotfix"` y en ella, corrige un error crítico en el archivo `"index.html"`. (Por ejemplo, añade el enlace a la nueva página about.html)

    Creamos la rama y nos cambiamos a ella:

    ```bash
    $ git branch hotfix
    $ git checkout hotfix
    ```

    Entramos con nano en el archivo y hacemos el cambio que nos indican

    ```bash
    $ nano index.html
    ```

    Añadimos los cambios y hacemos el commit 

    ```bash
    $ git add index.html
    $ git commit -m "Añadido enlace a about.html en index.html"
    $ git status
    ```

    

15. Fusiona la rama `"hotfix"` con la rama principal y verifica el historial de commits de forma que se vean todas las ramas gráficamente. ¿Borrarías la rama `hotfix`? ¿En qué caso? ¿Cómo?

    Nos cambiamos a la rama main:

    ```bash
    $ git checkout main
    ```

    Fusionamos las ramas:

    ```bash
    $ git merge hotfix
    ```

    Mostramos el historial de los logs:

    ```bash
    $ git log --all --decorate --oneline --graph
    ```

    ![Captura de pantalla 2025-10-17 a las 11.40.28](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/Captura%20de%20pantalla%202025-10-17%20a%20las%2011.40.28.png)

    

    Borraría la rama porque ya se fusionó y no es necesaria ya que era una corrección rápida de un error critico. Esto evita que halla errores por ver muchas ramas de este tipo, una vez solucinado el problema ya no hacen falta.

    ```bash
    $ git branch -d hotfix
    ```

    Podemos verificar que se ha borrado con:

    ```bash
    $ git branch
    ```

    

16. Muestra el historial de cambios limitado a los últimos 3 commits.

    ```bash
    $ git log -3 --oneline
    ```

    ![Captura de pantalla 2025-10-17 a las 11.43.31](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/Captura%20de%20pantalla%202025-10-17%20a%20las%2011.43.31.png)

    

17. Etiqueta el commit actual como "v1.0" y muestra las etiquetas existentes.

    ```bash
    $ git tag -a v1.0 -m "Versión 1.0 del proyecto Forty"
    ```

    O de forma mas simple:

    ```bash
    $ git tag v1.0
    ```

    Para visualizar que se ha realizado la etiqueta con éxito lo comprobamos con uno de estos dos comandos:

    ```bash
    $ git tag             //Nos da la versión (v1.0)
    $ git show v1.0       // Nos muestra mas detalles incluido el comentario 
    ```



------



## Trabajo en remoto

> Antes de nada es necesario crear un repositorio en GitHub llamado `"forty"` y no debemos crear el README.md en el remoto. Una vez creado esto se nos dará una URL con la dirección de nuestro nuevo repositorio.

1. Sube al remoto los ficheros de tu repositorio local

   Una vez creado nuestro repositorio llamando `forty`:

   - Conectamos nuestro local con el remoto desde nuestra consola

     ```bash
     $ git remote add origin https://github.com/CrisMunizMarin/Forty.git
     ```

     

   - Subimos los archivos al repositorio

     ```bash
     $ git push -u origin main
     ```

     

   - Subimos la tag que habiamos creado

     ```bash
     $ git push origin --tags
     ```

     

2. En local, crea una rama 'feature-head'. Cambia el título en la sección del head de index.html, borra los comentarios del  head , o previos, también. Confirma y sube los cambios al remoto.

   ```bash
   $ git checkout -b feature-head
   ```

   - Ahora realizamos los cambios en el index.html

   - Añadimos los cambios y hacemos commit y también subimos la nueva rama al remoto

     ```bash
     $ git add index.html
     $ git commit -m "Cambios en el index.html: Borrado de Title y comentarios previos al HEAD"
     $ git push -u origin feature-head
     ```

     

3. En remoto, crea una rama 'feature-articulo'. Duplica la página generic , nómbrala como  articulo.html, y añade como contenido un artículo sobre Git. Confirma los cambios y realiza un commit. Muestra los commits del repositorio tal como se ven en GitHub.

   - Nos vamos a GitHub y creamosuna nueva rama

     <img src="./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/Captura%20de%20pantalla%202025-10-24%20a%20las%209.27.59.png" alt="Captura de pantalla 2025-10-24 a las 9.27.59" style="zoom: 67%;" />
     
     

   - Creamos articulo.html: 

     Vamos al archivo genérico.html, hacemos click en RAW y copiamos todo el contenido. Vamos a la vista principal y añadimos un fichero y lo llamamos articulo.html y pegamos lo que hemos copiado.

     <u>Add file > Create new file < introducimos lo que queremos  y lo nombramos</u> 

     ![Captura de pantalla 2025-10-24 a las 9.33.12](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/Captura%20de%20pantalla%202025-10-24%20a%20las%209.33.12.png)

   - Hacemos el cambio que nos piden

     ![Captura de pantalla 2025-10-23 a las 13.59.00](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/Captura%20de%20pantalla%202025-10-23%20a%20las%2013.59.00.png)

   - Confirmamos los cambios desde el propio GitHub

     <img src="./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/image-20251023140655709.png" alt="image-20251023140655709" style="zoom:67%;" />

   - Commits

     ![image-20251023141130221](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/image-20251023141130221.png)

4. En el repositorio local  examina los cambios. Actualiza el repositorio con el remoto. Fusiona en 'main' las dos ramas 'feature'. Crea la etiqueta 'v2.0'. Muestra los logs, commits, etiquetas y ramas actuales, en local y en remoto

   - volvemos a main

     ```bash
     $ git checkout main
     ```

     

   - Nos traemos los cambios del remoto al local

     ```bash
     $ git pull
     ```

     

   - fusionamos las ramas a main

     ```bash
     $ git merge feature-head
     $ git merge feature-articulo
     ```

     

   - Creamos etiquetas v2.0

     ```bash
      $ git tag -a v2.0 -m "Version 2.0 con nuevas funcionalidades de head y articulo"
     ```

     

   - Mostramos los logs en local y remoto

   - ```bash
     $ git log --all --decorate --oneline --graph
     ```

     ![image-20251023141927205](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/image-20251023141927205.png)

     ```bash
     $ git tag
     ```

     ![image-20251023142122620](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/image-20251023142122620.png)

     ```bash
     $ git branch -a
     ```

     ![image-20251023142223762](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/image-20251023142223762.png)

     

5. En tu copia local, crea una rama nueva.  En la rama nueva, cambia los enlaces de la página index.html para que apunten correctamente a la nueva página cambios.

   - Crear rama correccion-enlaces

     ```bash
     $ git checkout -b correccion-enlaces
     ```

     

   - Hacemos cambios en índex.html (En mi caso he sustituido ele enlace que apuntaba a generic.html por articulo.html)

     <img src="./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/Captura%20de%20pantalla%202025-10-24%20a%20las%2010.02.31.png" alt="Captura de pantalla 2025-10-24 a las 10.02.31" style="zoom:67%;" />

   - Añadimos los cambios y realizamos el commit

     ```bash
     $ git add index.html
     ```

     ```bash
     $ git commit -m "Sustitución de enlace generic.html por articulo.html"
     ```

     

6. Muestra los logs de forma que se vean las ramas en tu copia local.  

   - Mostramos los logs en local

     ```bash
     $ git log --all --decorate --oneline --graph
     ```

     ![image-20251024100956097](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/image-20251024100956097.png)

   - Volvemos a la rama main

     ```bash
     $ git checkout main
     ```

     Nos avisa que tenemos que subir los cambios que hemos realizado con la rama corrección-enlaces

     

     

7. Te gusta el resultado de los cambios. Incorpora los cambios de la rama nueva a la principal.

   - Fusionamos las ramas

     ```bash
     $ git merge correccion-enlaces
     ```

     ![image-20251024101522814](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/image-20251024101522814.png)

     

8. Sube los cambios al remoto borrando la rama nueva, si es necesario. Comprueba primero con un comando en local, las ramas que hay en el repositorio remoto. 

   - Subimos los cambios a la rama main del remoto

     ```bash
     $ git push
     ```

     

   - Comprobamos las ramas que tenemos en remoto para verificar que se han subido correctamente

     ```bash
     $ git branch -r
     ```

     ![image-20251024103939396](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/image-20251024103939396.png)

     Aqui como se puede ver he cometido un error ya que no habia subido la rama al remoto con `git push -u origin corrección-enlaces` por lo que no aparece en remoto pero si en local, asique solo borrare la rama en local y podre continuar con el ejercicio.

     ![image-20251024104349355](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/image-20251024104349355.png)

     ```bash
     $ git branch -d correccion-enlaces
     ```

     ![image-20251024104538588](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/image-20251024104538588.png)

     ![image-20251024104611326](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/image-20251024104611326.png)

     

9. Muestra en local  los cambios en el archivo index.html entre la versión actual y la anterior.

   ```bash
   $ git diff HEAD~1 HEAD index.html
   ```

   ![image-20251024105535756](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/image-20251024105535756.png)

   

10. En el repositorio en GitHub, navega hasta el archivo index.html y selecciona la opción "History".

![image-20251024105707133](./01%20-%20Ejercicio%20de%20Git%20-%20Forty%20-%20local%20y%20remoto.assets/image-20251024105707133.png)

