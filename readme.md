####1.¿Qué comando utilizaste en el paso 11? ¿Por qué?
	git reset --hard HEAD~1
	
He utilizado reset para deshacer cambios, --hard
	para perder los cambios del working copy y HEAD~1
	para volver al padre.
	
####2. ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
	git reflog
	git reset --hard 50db5c3
	
He utilizado reflog para buscar el commit que
queríamos, y he vuelto a usar reset --hard para
volver a él perdiendo los cambios del working copy
y por tanto quedándome en el mismo estado.
	
####3. El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
No causó ningún conflicto ya que en master no existian
	cambios posteriores a cuándo se creó la rama htmlify.
####4. El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
Sí. Porque el fichero poem.md había sido modificado en las mismas líneas en las dos ramas y git no sabe cómo resolver el conflicto.

####5. El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No, ya que el fichero no había sufrido modificaciones en la rama master. Solo había que incorporar los cambios de la rama htmlify.

####6. ¿Qué comando o comandos utilizaste en el paso 25?
	git log --graph --decorate --pretty=oneline

####7. El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
Sí. Porque master y title forman una lista. El puntero de master puede pasar a apuntar a title sin dejar ningún commit innaccesible.

####8. ¿Qué comando o comandos utilizaste en el paso 27?
	git reset HEAD~1
	
####9. ¿Qué comando o comandos utilizaste en el paso 28?
	git checkout -- poem.md
	
####10. ¿Qué comando o comandos utilizaste en el paso 29?
	git branch -D title

####11. ¿Qué comando o comandos utilizaste en el paso 30?
	git reflog y buscamos el commit
	git reset --hard c3b501c

####12. ¿Qué comando o comandos usaste en el paso 32?
	git reflog y buscamos el commit
	git reset --hard b29c625
Podríamos haber usado git checkout pero haciéndolo así solo
movemos el puntero HEAD dejándolo en un estado detached y no moviendo el puntero de la rama.
	
####13. ¿Qué comando o comandos usaste en el punto 33?
	git reflog y buscamos el commit
	git reset --hard c3b501c
	
Podríamos haber usado git checkout pero haciéndolo así 
solo movemos el puntero HEAD dejándolo en un estado 
detached y en este caso es peor porque si ejecutamos 
git branch no estamos en master ya que HEAD apunta
a un commit en concreto y no al puntero de la rama
master (aunque coincida que sea el mismo commit).
	
