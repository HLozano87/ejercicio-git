- ¿Qué comando utilizaste en el paso 11? ¿Por qué?

    * `git reset --hard HEAD~1` :  Mueve el puntero un paso atrás y hace que todos los cambios que hayan después del mismo se pierdan.

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

    * `git reflog`: para recuperar del historial el hash del commit borrado.
    * `git reset --hard <hash>` : Recupera el commit señalando al hash y recuperando su contenido y estado.

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

    * No causa conflicto porque el HEAD apunta a styled que tiene nuevos commits con los cambios que ya tenia main. Como desde el ultimo cambio main no tuvo ningún avance, styled absorbe a main sin conflicto ya que ya tiene todos sus cambios.

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

    * Si. El problema es que htmlify modificó los cambios iniciales de main al crearse la rama desde allí, sigue estando en el origen, main no tenia los cambios de styled que está su HEAD un paso mas atrás, y al intentar styled absorber a htmlify tiene modificaciones en las mismas líneas que ya tenia absorbida de main y causa conflicto.

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

    * No, porque en un inicio styled tenia mergeados los cambios originales de main que sigue sin tener ningún nuevo cambio. Esto hace que al hacer un `merge` haga un fast forward integrando los cambios que habían en styled a main sin causar conflictos.

- ¿Qué comando o comandos utilizaste en el paso 25?

     * `git log --graph --oneline`: Genera un gráfico del historial de los commits del repositorio, permitiendo ver el flujo de trabajo. 

    ```
    *   c5e96c9 (origin/styled) Resolucion de conflictos, mantenemos styled
    |\
    | * 0d59323 (tag: htmlify, origin/htmlify) style: Cambia el formato a estilo HMTL en git-nuestro.md
    * | 4dc63c8 docs: Puntos 11, 12 y 13 del enunciado
    * | c76ee25 (tag: styled) style: Cambio de estilo en el formato de palabras claves
    |/
    * 312b635 (tag: inicial) first commit
    ```

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
    
    * Sí, porque la rama main no se había modificado nuevamente desde el ultimo merge con styled. Aunque un `merge --no-ff` ofrece claridad en el historial al tener que hacer un commit ya que el fast forward no crea un commit.

- ¿Qué comando o comandos utilizaste en el paso 27?

    * `git reset --soft HEAD~1`: deshace el merge y mantiene los cambios en el working copy.

- ¿Qué comando o comandos utilizaste en el paso 28?

    * `git restore --stage y git restore <archivo>`

- ¿Qué comando o comandos utilizaste en el paso 29?

    * `git branch -D title`

- ¿Qué comando o comandos utilizaste en el paso 30?

    * `git reflog`
    * `git checkout <hash>`
    * `git switch -c title` 
    * `git checkout main` 
    * `git merge --no-ff title`

    Con `git reset --hard <hash>` para rehacerlo podría haberlo hecho pero no quedaría ningún commit como referencia en el historial.

- ¿Qué comando o comandos usaste en el paso 32?

    * `git log --oneline` para buscar el hash
    * `git checkout <hash>` para mover el HEAD.

- ¿Qué comando o comandos usaste en el punto 33?

    * `git switch -` para llevar el HEAD al estado actual.