- ¿Qué comando utilizaste en el paso 11? ¿Por qué?

    * `git reset --hard HEAD~1` :  Mueve el puntero un paso atrás y hace que todos los cambios que hayan después del mismo se pierdan.

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

    * `git reset --hard <hash>` : Recupera el commit señalando al hash y recuperando su contenido y estado.

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

    * No causa conflicto porque fue un merge fast forward, no hubieron commits y los cambios al ser de estilo (itálicas y backticks) git no lo considera conflicto para un merge.

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

    * Si, porque se estaban sobrescribiendo las mismas líneas.

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

    * No, porque los conflictos se resolvieron en el `merge` de styled.

- ¿Qué comando o comandos utilizaste en el paso 25?

    * `git log --graph --oneline` y `git log --graph`: Genera un gráfico representando información de los movimientos del repositorio. Es visualmente más cómodo que si uso `git log --graph`. Depende del contexto se puede usar un comando u otro, aunque este último muestra más información.

    ```
    * 761fdb7 (HEAD) Punto 25 del enunciado
    * de83d26 docs: Puntos 19 y 21 del enunciado
    *   c5e96c9 (origin/styled) Resolucion de conflictos, mantenemos styled
    |\
    | * 0d59323 (tag: htmlify, origin/htmlify) style: Cambia el formato a estilo HMTL en git-nuestro.md
    * | 4dc63c8 docs: Puntos 11, 12 y 13 del enunciado
    * | c76ee25 (tag: styled) style: Cambio de estilo en el formato de palabras claves
    |/
    * 312b635 (tag: inicial) first commit
    ```

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

    * Sí, porque la rama main no se había modificado nuevamente desde el ultimo merge con styled.

- ¿Qué comando o comandos utilizaste en el paso 27?

    * `git reset --soft HEAD~1`: deshace el merge y mantiene los cambios en el working copy.

- ¿Qué comando o comandos utilizaste en el paso 28?

    * `git restore --stage y git restore <archivo>`

- ¿Qué comando o comandos utilizaste en el paso 29?

    * `git branch -D title`

- ¿Qué comando o comandos utilizaste en el paso 30?

    * `git reflog` para buscar el hash y `git reset --hard <hash>` para rehacerlo.

- ¿Qué comando o comandos usaste en el paso 32?

    * `git log --oneline` para buscar el hash y  `git checkout <hash>` para mover el HEAD.

- ¿Qué comando o comandos usaste en el punto 33?

    * `git switch -` para llevar el HEAD al estado actual.