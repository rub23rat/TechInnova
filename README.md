## Ruben David Rat
## Lenguaje de Marcas
## IES Aguadulce 2023-2024
## https://rub23rat.github.io/TechInnova/

### Uso de Git mediante la terminal git bash. Las instrucciones y sus resultados deben mostrar como bloques de código markdown:

1. Configuración de usuario
    
    Antes de crear el repositorio hay que crear al usuario de este:

    Primero se debe establecer el nombre del usuario:
    ```
    rub11@DESKTOP-L84U2DO MINGW64 ~/Documents/TechInnova (master)
    $ git config --global user.name "Ruben Rat"
    ```
    Después, se debe establecer el correo de este usuario
    ```
    rub11@DESKTOP-L84U2DO MINGW64 ~/Documents/TechInnova (master)
    $ git config --global user.email "rubenrat@gmail.com"
    ```

1. Creación del repositorio en nuestro ordenador (init)
    
    Estando en la ruta en la que queremos que esté nuestro repositorio ponemos el siguiente comando y se creará:
    ```
    git init TechInnova
    ```
    A continuación nos metemos dentro:
    ```
    cd TechInnova
    ```

1.  Creación de un commit inicial (add, status, commit, log)

    Estando dentro de la ruta en la que se encuentre nuestro repositorio creamos el archivo "readme". Una vez ya creado se procederá a abrir vscode habriendose desde nuestro repositorio. Al final añadimos el archivo "readme" a nuestro git.
    ```
    touch README.md
    code . &
    git add README.md
    ```
    Vemos el estado de git:
    ```
    $ git status
    On branch master

    No commits yet

    Changes to be committed:
    (use "git rm --cached <file>..." to unstage)
            new file:   README.md
    ```
    En el caso anterior me estaba diciendo que aun no he realizado copias de seguridad por lo cual ahora realizaremos esa copia de seguridad:
    ```
    rub11@DESKTOP-L84U2DO MINGW64 ~/Documents/TechInnova (master)
    $ git commit -m README.md
        [master (root-commit) bac41f2] README.md
        2 files changed, 42 insertions(+)
        create mode 100644 README.md
        create mode 100644 capturas/Imagen1.png
    ```
    A continuación vemos las copias de seguridad que hemos realizado de esta forma:
    ```
    rub11@DESKTOP-L84U2DO MINGW64 ~/Documents/TechInnova (master)
    $ git log
    commit 3d9c640129bc05108034fa11aa13e034e6439762 (HEAD -> master)
    Author: Ruben Rat <rubenrat@gmail.com>
    Date:   Thu Jan 18 08:58:59 2024 +0100

        README.md

    commit bac41f2c25d5e65d262d5e02b17612f62abbc03d
    Author: Ruben Rat <rubenrat@gmail.com>
    Date:   Thu Jan 18 08:53:46 2024 +0100

        README.md

    ```

1.  Creación del repositorio en Github
    
    Establecemos el nombre de nuestro repositorio en GitHub y lo creamos:

    ![](/capturas/Imagen1.png)

    Añado al colaborador de mi repositorio:

    ![](/capturas/imagen7.png)

1. Añadir el remoto al repositorio local (branch, remote)

    De esta forma añado de forma remota a mi repositorio local:
    ```
    rub11@DESKTOP-L84U2DO MINGW64 ~/Documents/TechInnova (master)
    $ git branch -M main
    ```

1. Subir el repositorio a Github (push)

    Para subir nuestro repositorio a GitHub debemos conectarlo con este. Tenemos la suerte de que GitHub nos facilite esta conexión remota mediante un enlace que ellos mismos la otorgan. Primero de todo establecemos la conexión con GitHub con el enlace personalizado de cada uno y después subimos nuestro repositorio a GitHub: 
    ```
    rub11@DESKTOP-L84U2DO MINGW64 ~/Documents/TechInnova (main)
    $ git remote add origin https://github.com/rub23rat/TechInnova.git

    rub11@DESKTOP-L84U2DO MINGW64 ~/Documents/TechInnova (main)
    $ git push -u origin main
        Enumerating objects: 11, done.
        Counting objects: 100% (11/11), done.
        Delta compression using up to 8 threads
        Compressing objects: 100% (10/10), done.
        Writing objects: 100% (11/11), 128.47 KiB | 11.68 MiB/s, done.
        Total 11 (delta 2), reused 0 (delta 0), pack-reused 0
        remote: Resolving deltas: 100% (2/2), done.
        To https://github.com/rub23rat/TechInnova.git
        * [new branch]      main -> main
        branch 'main' set up to track 'origin/main'.
    ```

1. Comprobar que está subido a Github

    Una vez realizada la conexión y subido nuestro repositorio, podemos observar que se encuentran nuestros archivos creados posteriormente:
    ![](/capturas/Imagen2.png)

### Publicación en Github Pages

1. Configurar el repositorio para que publique el directorio raíz en Github Pages
    
    Debemos ir a la parte de ajustes de nuestro repositorio y entrando en el apartado "pages", elegimos la rama y el directorio raiz. Por ultimo queda guardar los cambios:
    ![](/capturas/imagen3.png)

1. Mostrar los despliegues (deployments)
    
    Antes de nada se recomienda crear un archivo index.html con algo de contenido dentro de este y a continuación hacer una copia de seguridad de todos los archivos y subirlo a nuestro repositorio:
    ```
    rub11@DESKTOP-L84U2DO MINGW64 ~/Documents/TechInnova (main)
    $ git add .

    rub11@DESKTOP-L84U2DO MINGW64 ~/Documents/TechInnova (main)
    $ git commit -m .
    [main 9a81b12] .
    4 files changed, 47 insertions(+), 1 deletion(-)
    create mode 100644 capturas/Imagen2.png
    create mode 100644 capturas/imagen3.png
    create mode 100644 index.html

    rub11@DESKTOP-L84U2DO MINGW64 ~/Documents/TechInnova (main)
    $ git status
    On branch main
    Your branch is ahead of 'origin/main' by 1 commit.
    (use "git push" to publish your local commits)

    nothing to commit, working tree clean
    ```
    Para ver los despliegues, en el apartado de "code" vemos que se encuentra en la parte de la derecha:
    ![](/capturas/imagen13.png)

    Una vez dentro podremos ver los despliegues:

    ![](/capturas/imagen9.png)

1. Mostrar la página web

    Al tener nuestro index subido y nuestro enlace ya creado de GitHub Pages podemos acceder a nuestro index con el enlace:

    ![](/capturas/imagen5.png)

1. Añadir en el primer apartado, Identificación, el enlace a la publicación del sitio web

    Aqui ponemos nuestro enlace para ver nuestra página:
    ![](/capturas/imagen6.png)

### Uso de Git mediante la interfaz de VSCode

1. Creación de otro commit

    Para hacer un commit debemos de ir al apartado que esta en la parte izquierda. Una vez ahí

    ![](/capturas/imagen8.png)

1. Subir el repositorio a Github

    ![](/capturas/imagen10.png)

1. Comprobar que está subido a Github

    ![](/capturas/imagen11.png)

1. Ver el listado de commit desde Github

    ![](/capturas/imagen12.png)

