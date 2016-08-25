## Diferencias entre git reset --mixed y git reset --soft

Cuando tu modificas un archivo en tu repositorio, el cambio es inicialmente unstaged. En orden del commit, tu deberias ponerlo en la etapa es decir, agregarlo al index usando git add. Cuando tu haces commit, los cambios que son commited seran agregadas al index.

--soft: Con esta opción estamos indicando que retrocedemos a el commit HEAD~1 y no perdemos los cambios de los commits posteriores, como lo mencionamos desharemos el commit y pondremos los archivos de nuevo en el stage.
No toca el archivo de índice o el árbol de trabajo en absoluto (pero restablece la cabeza a *<commit>* , al igual que todos los modos de hacer ). Esta deja todos sus archivos modificados "Los cambios que sean en commited", como *git status* lo pondría. Cuando se corre git reset --soft B, master (y por lo tanto HEAD) ahora apunta a B , pero el índice todavía tiene los cambios de C; git status mostrará como por etapas. Así que si corremos git commit en este punto , vamos a tener un nuevo commit con los mismos cambios que C.

![alt text](https://github.com/Oswaldofm17/Diff-mixed-and-soft/blob/master/soft.jpg "Logo Title Text 1")


--mixed: Restablece el índice pero no el árbol de trabajo (es decir, los cambios de los archivos se conservan pero no marcados para el *commit*) e informa que no ha sido actualizada. Esta es la acción por defecto.

![alt text](https://github.com/Oswaldofm17/Diff-mixed-and-soft/blob/master/reset.png "Logo Title Text 2")
