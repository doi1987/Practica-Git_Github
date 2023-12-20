
- ¿Qué comando utilizaste en el paso 11? ¿Por qué?
    git reset HEAD~1
        Deshacemos el último commit
    git restore git-nuestro.md
        Deshacemos los cambios hasta antes del commit y se queda el archivo git-nuestro.md como la primera vez que lo subimos
- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
    git reflog
        Buscamos la referencia del ultimo movimiento hecho antes de desactualizarlo y lo copiamos
    git reset <referencia copiada anteriormente>    
        movemos la rama styled al commit anteriormente "borrado"
    git status
        comprobamos que son diferentes el git-nuestro.md del working con el que está en el commit
    git restore git-nuestro.md
        restauramos el archivo git-nuestro.md como si no hubiésemos hecho el paso 11 y lo comprobamos en nuestro working area
    
- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
    git merge main
        No causo ningún conflicto al ser un fast forward. La rama styled ya contenía a la rama main. 
        Gráficamente el commit B(rama styled) es el hijo del commit A(rama main). B -> A
- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
    git checkout styled
        Primero nos movemos a la rama styled que es la que queremos que absorba a htmlify
    git merge htmlify
        Existe un conflicto porque los git-nuestro.md son distintos. 

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
    git checkout main
        Nos cambiamos a la rama main
    git merge styled
        No genera ningún conflicto

- ¿Qué comando o comandos utilizaste en el paso 25?
    git log --graph

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
    Se podría hacer un fast forward porque la rama title ya contenía a la rama main

- ¿Qué comando o comandos utilizaste en el paso 27?
    git reset HEAD~1

- ¿Qué comando o comandos utilizaste en el paso 28?
    git restore git-nuestro.md

- ¿Qué comando o comandos utilizaste en el paso 29?
    git branch -d title
        No nos deja hacerlo porque hay no se ha hecho merge en la rama title y se perderían cambios

- ¿Qué comando o comandos utilizaste en el paso 30?
    git merge title

- ¿Qué comando o comandos usaste en el paso 32?
    git log 
        Lo usamos para copiar la referencia del primer commit
    git reset "referencia"

- ¿Qué comando o comandos usaste en el punto 33?
    git reflog 
        Lo usamos para encontrar la referencia del estado final de los commits
    git reset "referencia
    