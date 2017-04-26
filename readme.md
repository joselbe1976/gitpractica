** - ¿Qué comando utilizaste en el paso 11? ¿Por qué? **

git reset --hard HEAD~1

Para apuntar al commit Styledanterior deshaciendo el ultimo commit  y quedando todo con el primer commit en Master inicial. Master y Styled apuntan al mismo commit.


** - ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué? **

git reset --hard ff9e5c0

Para hacer esto mediante git reflog, veo el commit que hice en la rama styled y con el hash posiciono  styled en ese commit, recuperando el trabajo. --hard para que me machaque el working copy



**- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**
 1. Me posiciono en maste primero: *git checkout styled*
 2. Hacemos el merge: *git merge master*

 No hace nada ni hay conflicto, "Already up-to-date"



**- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué? **
git checkout styled
git merge htmlify

Genero un conflicto que habia que solucionar eliminando del fichero la patrte de abajo que añlade,nos quedamos parte superior. Al final git commit, sale el fichero y Control+X


**- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué? **

git checkout master
git merge styled

No genero ningun conflicto porque se ha realizado un fast forward, eso se debe a que Master no ha tenido commit posteriores al crear la rama styled. por lo que realmente se ha movido al commit final de styled.


**- ¿Qué comando o comandos utilizaste en el paso 25?**

git log --graph --decorate --pretty=oneline

**- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué? **

git merge --no-ff title

Si podría ser porque en Master teniamos el mismo contenido que title, y en title solo habiamos añadido el titulo, por lo que se podría realizar un FF

**- ¿Qué comando o comandos utilizaste en el paso 27?**

git reset HEAD~1

**- ¿Qué comando o comandos utilizaste en el paso 28? **

git checkout git-nuestro.md

**- ¿Qué comando o comandos utilizaste en el paso 29? **

git branch -D title

**- ¿Qué comando o comandos utilizaste en el paso 30? **
Primero se busca el reflog y posiciono  al ultinmo commit del merge

git reset --hard 850404f


**- ¿Qué comando o comandos usaste en el paso 32?**

git reset --hard 02c34ce


**- ¿Qué comando o comandos usaste en el punto 33?**

git reset --hard 850404f



