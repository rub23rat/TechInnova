## Ruben David Rat
## Lenguaje de Marcas
## IES Aguadulce 2023-2024
## https://rub23rat.github.io/TechInnova/

### Uso de Git mediante la terminal git bash. Las instrucciones y sus resultados deben mostrar como bloques de código markdown:

1. Configuración de usuario
    
    Antes de crear el repositorio creo a los usuarios
    ```
    rub11@DESKTOP-L84U2DO MINGW64 ~/Documents/TechInnova (master)
    $ git config --global user.name "Ruben Rat"

    rub11@DESKTOP-L84U2DO MINGW64 ~/Documents/TechInnova (master)
    $ git config --global user.email "rubenrat@gmail.com"
    ```

1. Creación del repositorio en nuestro ordenador (init)
    
    
    ```
    git init TechInnova
    cd TechInnova
    ```

1.  Creación de un commit inicial (add, status, commit, log)
    ```
    touch README.md
    code . &
    git add README.md
    ```

    ```
    $ git status
    On branch master

    No commits yet

    Changes to be committed:
    (use "git rm --cached <file>..." to unstage)
            new file:   README.md
    ```
    ```
    rub11@DESKTOP-L84U2DO MINGW64 ~/Documents/TechInnova (master)
    $ git commit -m README.md
        [master (root-commit) bac41f2] README.md
        2 files changed, 42 insertions(+)
        create mode 100644 README.md
        create mode 100644 capturas/Imagen1.png
    ```
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
    ![](/capturas/Imagen1.png)
    ![](/capturas/imagen7.png)

1. Añadir el remoto al repositorio local (branch, remote)
    ```
    rub11@DESKTOP-L84U2DO MINGW64 ~/Documents/TechInnova (master)
    $ git branch -M main
    ```

1. Subir el repositorio a Github (push)
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
    ![](/capturas/Imagen2.png)

### Publicación en Github Pages

1. Configurar el repositorio para que publique el directorio raíz en Github Pages
    ![](/capturas/imagen3.png)

1. Mostrar los despliegues (deployments)
    
    Antes de nada hay que hacer un commit de todos los archivos y a continuación publicarlo a nuestro repositorio:
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
    ![](/capturas/imagen4.png)

1. Mostrar la página web

    ![](/capturas/imagen5.png)

1. Añadir en el primer apartado, Identificación, el enlace a la publicación del sitio web
    ![](/capturas/imagen6.png)

### Uso de Git mediante la interfaz de VSCode

1. Creación de otro commit

    ![](/capturas/imagen8.png)

1. Subir el repositorio a Github
    