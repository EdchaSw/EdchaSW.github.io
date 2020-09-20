## Prueba de fetch para ver como funciona se supone que los pasos son los siguientes.

1. alguien subio este archivo al repositorio remoto

2. se ejecutaran los siguientes pasos con `git fetch`

 Sincronización del origen con git fetch

En el siguiente ejemplo se describe el flujo de trabajo habitual de sincronización del repositorio local con la rama maestra del repositorio central.

git fetch origin

Así se muestran las ramas que se han descargado:

a1e8fb5..45e66a4 master -> origin/master
a1e8fb5..9e8ab1c develop -> origin/develop
* [new branch] some-feature -> origin/some-feature

The commits from these new remote branches are shown as squares instead of circles in the diagram below. As you can see, git fetch gives you access to the entire branch structure of another repository.




Para ver qué commits se han añadido a la rama maestra de nivel superior, puedes ejecutar un comando git log con el filtro origin/master:

git log --oneline master..origin/master

Para aprobar los cambios y fusionarlos con tu rama maestra local, usa estos comandos:

git checkout master
git log origin/master

A continuación podemos usar el comando git merge origin/master:

git merge origin/master

Las ramas origin/master y master ahora apuntan al mismo commit y están sincronizadas con los desarrollos de nivel superior.
