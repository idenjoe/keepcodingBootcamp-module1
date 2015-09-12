####1.¿Qué comando utilizaste en el paso 11? ¿Por qué?
	git reset --hard HEAD~1
	
He utilizado reset para deshacer cambios, --hard
	para perder los cambios del working copy y HEAD~1
	para volver al anterior.
	
####2. ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
	git reset --hard 50db5c3
	
He utilizado reflog para buscar el commit que
	queríamos, y he vuelto a usar reset --hard para
	volver a él perdiendo los cambios del working copy
	y por tanto quedándome en el mismo estado.
	
####3. El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
No causó ningún conflicto ya que en master no existian
	cambios posteriores a cuándo se creó la rama htmlify
	y por tanto no había nada que mergear.
####4. El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
Sí. Porque el fichero poem.md había sido modificado en las mismas líneas en las dos ramas y git no sabe cómo resolver el conflicto.

####5. El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
Sí, porque el fichero había cambiado desde la última versión aunque git lo ha sabido resolver sin necesidad de hacerlo manualmente.

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
	git reset --hard c3b501c

####12. ¿Qué comando o comandos usaste en el paso 32?
	git reset --hard b29c625
	
####13. ¿Qué comando o comandos usaste en el punto 33?
	git reset --hard c3b501c
	
