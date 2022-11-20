## PRACTICA 1 GIT

Tomado de https://github.com/asanzdiego/curso-nivelacion-bigdata-2017/blob/master/ejercicios/ejercicios-git-github-markdown-solucion.md

#### **Crear repositorio**

1. Crear un repositorio en vuestro GitHub llamado Practica1Softca

2. Clonar vuestro repositorio en local.

` git clone url`: Nos permite crear nuestro repositorio de github

#### **README**

3. Crear (si no lo habéis creado ya) en vuestro repositorio local
un documento README.md.

#### **Commit inicial**

4. Añadir al README.md los comandos utilizados hasta ahora y hacer un commit inicial con el mensaje commit inicial.

    `code README.md`: Para abrir un editor y agregar contenido
	
    `git status`: por buena práctica para ver si se han modificado y a cuál archivo

    `git commit am- "commit inicial"`: Con este comando agragamos al Staging y hacemos commit, es decir lo guardamos en el repositorio local
	
    `git status:` por buena práctica para revisar que no se nos quedó algo por guardar.

#### **Push inicial**

5. Subir los cambios al repositorio remoto.

`$ git push origin master`

#### **Ignorar archivos**

6. Crear en el repositorio local un fichero llamado privado.txt.

`touch privado.txt`

7. Crear en el repositorio local una carpeta llamada privada.

` mkdir privada`

8. Realizar los cambios oportunos para que tanto el archivo como la carpeta sea ignorada por git.

`touch .gitignore`

`code .gitignore`: Escribimos (linea por linea) los nombres de carpetas y arhivos que queremos ignorar

`git add .gitignore`

`git commit -m "carpeta para ignorar archivos"`

#### **Añadir fichero 1.txt**

9. Añadir fichero 1.txt al repositorio local.

`touch 1.txt`

#### **Crear el tag v0.1**

10. Crear un tag v0.1.

`git log --all --graph --decorate --online`: Para ver de manera resuimida los commits (debemos copear el commit de interes para hacer el tag)

` git tag -a V0.1 -m "Primera parte" b232be5`

#### **Subir el tag v0.1**

11. Subir los cambios al repositorio remoto.

`git push origin --tags`

#### **Crear una rama v0.2**

12.. Crear una rama v0.2.

`git branch V0.2`

13. Posiciona tu carpeta de trabajo en esta rama.

`git checkout V0.2`

#### **Añadir fichero 2.txt**

14. Añadir un fichero 2.txt en la rama v0.2.

` touch 2.txt`

#### **Crear rama remota v0.2**

15. Subir los cambios al repositorio remoto.

`git push origin V0.2`

16. Posicionarse en la rama master.

` git checkout master`

#### **Merge directo**

17.Hacer un merge de la rama v0.2 en la rama master.

`git merge V0.2`

#### **Merge con conflicto**

18. En la rama master poner Hola en el fichero 1.txt y hacer commit.

19. Posicionarse en la rama v0.2 y poner Adios en el fichero &quot;1.txt&quot; y hacer commit.

20. Posicionarse de nuevo en la rama master y hacer un merge con la rama v0.2

####**Arreglar conflicto**

22. Arreglar el conflicto anterior y hacer un commit.

####**Borrar rama**

23. Crear un tag v0.2

`git tag -a v0.2 -m "parte 2" 31b360c`

24. Borrar la rama v0.2

`git branch -D V0.2`