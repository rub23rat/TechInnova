## Ruben David Rat
## Lenguaje de Marcas
## IES Aguadulce 2023-2024
## Enlace a la web (Ver más abajo):

### Uso de Git mediante la terminal git bash. Las instrucciones y sus resultados deben mostrar como bloques de código markdown:

1. Configuración de usuario

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