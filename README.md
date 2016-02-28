## Diferencias entre git reset --mixed y git reset --soft

--soft: Con esta opción estamos indicando que retrocedemos a el commit HEAD~1 y no perdemos los cambios de los commits posteriores, como lo mencionamos desharemos el commit y pondremos los archivos de nuevo en el stage.
No toca el archivo de índice o el árbol de trabajo en absoluto (pero restablece la cabeza a *<commit>* , al igual que todos los modos de hacer ). Esta deja todos sus archivos modificados "Los cambios que sean en commited", como *git status* lo pondría .

--mixed: Restablece el índice pero no el árbol de trabajo (es decir, los cambios de los archivos se conservan pero no marcados para el *commit*) e informa que no ha sido actualizada. Esta es la acción por defecto.

![alt text](https://github.com/Oswaldofm17/Diff-mixed-and-soft/blob/master/reset.png "Logo Title Text 1")
