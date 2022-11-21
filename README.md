# ejercicioGit2
<!-- TODO: Ir completando cada punto con capturas y código -->

1. Creación de repositorio en GitHub, inicializándolo con un README.md y el .gitignore que GiHub ofrece para Java.

2. Modificación de este README.md desde GitHub para indicar lo dos primeros pasos.
3. Clono el repositorio
4. Creo un proyecto en ese directorio
5. ¡Ups! el proyecto se creó en una subcarpeta. Muevo su contenido al directorio raiz del repo.
6. Quiero volver al paso 3 para hacerlo bien. Hago un log

    ```sh
    avida@DESKTOP-EG6VTFK MINGW64 ~/TRABAJO/cd/IdeaProjects/ejercicioGit2 (main)
    $ git log --oneline
    b7d0342 (HEAD -> main, origin/main, origin/HEAD) moviendo el proyecto a la carpeta raiz del repo
    2f9b3d6 creando proyecto en intellij
    5ae4948 Update README.md
    7bec56f Initial commit
   ```

   Como quiero volver a antes de crear el proyecto, tengo que hacer un reset al commit previo (5ae4948). Al hacerlo, perdería los commits posteriores, así que creo una rama nueva para ello.

   ```bash
   avidaldo@W10N-I9E31 MINGW64 /e/Alejandro/cd/ejercicioGit2 (main)
    $ git branch rama2
    avidaldo@W10N-I9E31 MINGW64 /e/Alejandro/cd/ejercicioGit2 (main)
    $ git checkout rama2
    Switched to branch 'rama2'
   ```

(Para crear una rama y pasar directamente a ella se podría también hacer en un paso con "git checkout -b rama2").

Ahora ya puedo hacer el reset:
```bash
avidaldo@W10N-I9E31 MINGW64 /e/Alejandro/cd/ejercicioGit2 (rama2)
$ git reset --hard 5ae4
HEAD is now at 5ae4948 Update README.md
   ```

y crear el proyecto directamente en el directorio donde ya está el repo.

![](./img/2022-11-21 21_45_05-Window.png)