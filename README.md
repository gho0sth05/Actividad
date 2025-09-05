# Actividad
# comandos básicos de Git y GitHub.
Con mi grupo de trabajo Karen Gonzalez, Laura Fonseca , Juan Bocanegra vamos a mostar algunos de  los comandos básicos de Git y GitHub..
---

## 🔹 Configuración
```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@example.com"
git config --list          # Ver configuraciones
``` 
# 🔹 Crear o clonar repositorios
```bash
git init                   # Crear un repositorio local
git clone URL              # Clonar un repositorio remoto
git remote -v              # Ver conexiones remotas
git remote add origin URL  # Conectar repositorio remoto
git remote remove origin   # Eliminar remoto
``` 
# 🔹 Estado y seguimiento
```bash
git status                 # Ver estado del repositorio
git add archivo.txt        # Agregar archivo al stage
git add .                  # Agregar todos los archivos
git rm archivo.txt         # Eliminar archivo y registrar cambio
git mv viejo.txt nuevo.txt # Renombrar archivo en Git
``` 
# 🔹 Guardar cambios
```bash
git commit -m "Mensaje"          # Commit con mensaje corto
git commit -am "Mensaje"         # Add + commit en un paso (solo archivos ya trackeados)
git commit --amend               # Modificar último commit
```
# 🔹 Sincronización con GitHub
```bash
git push origin main             # Subir cambios
git push -u origin main          # Subir y establecer upstream
git pull origin main             # Descargar y fusionar cambios
git fetch                        # Descargar referencias sin fusionar
```
# 🔹 Ramas (branches)
###🔹 ¿Para qué sirven las ramas?
* Para trabajar en funcionalidades nuevas sin arruinar el código estable.
* Para que varias personas trabajen a la vez sin chocar.
* Para hacer pruebas o ideas sin miedo a dañar el proyecto.
```bash
git branch                       # Ver ramas
git branch nombre-rama           # Crear rama
git checkout nombre-rama         # Cambiar a rama
git checkout -b nombre-rama      # Crear y cambiar
git merge nombre-rama            # Fusionar rama actual con otra
git branch -d nombre-rama        # Eliminar rama
git switch nombre-rama           # Cambiar de rama (alternativa a checkout)
git switch -c nombre-rama        # Crear y cambiar de rama                      # Descargar referencias sin fusionar
```
# 🔹 Ayuda
```bash
git help                         # Ayuda general
git help <comando>               # Ayuda de un comando
```
<!-- Laura -->
## 🔹 Guardar y recuperar trabajo temporal (Stash)
```bash
git stash                # Guardar cambios en memoria temporal
git stash list           # Ver lista de stashes guardados
git stash pop            # Recuperar el último stash y aplicarlo
git stash drop           # Eliminar stash sin aplicarlo
``` 

## 🔹 Historial y revisión
```bash
git log                  # Ver historial de commits
git log --oneline        # Ver historial resumido
git show <id-commit>     # Ver detalles de un commit específico
``` 

## 🔹 Revertir y resetear cambios
```bash
git checkout -- archivo.txt      # Descartar cambios en un archivo
git reset archivo.txt            # Quitar archivo del stage
git reset --soft HEAD~1          # Eliminar el último commit (manteniendo cambios)
git reset --hard HEAD~1          # Eliminar commit y cambios
git revert <id-commit>           # Crear un commit que deshace otro
``` 

## 🔹 Resumen de comandos básicos
Estos son los más usados en el día a día:

```bash
bash
git status                   # Ver estado del repositorio
git add <archivo>            # Añadir un archivo al área de preparación (staging)
git commit -m "mensaje"      # Crear un commit con mensaje
git push                     # Subir cambios al repositorio remoto
git pull  
```

## 🔹 Buenas prácticas recomendadas
Commits pequeños y frecuentes: evita subir muchos cambios en un solo commit.

Ejemplo:

feat: agrega sección de ramas

fix: corrige error en configuración de usuario

docs: actualiza el README con comandos básicos
```bash

Actualizar tu rama antes de subir cambios:       # git pull origin main
```
<!-- Boca -->
## 🔹 Comparación de cambios
```bash
git diff                     # Ver cambios no preparados (working directory)
git diff --staged            # Ver cambios ya en el staging area
git diff <id1> <id2>         # Comparar dos commits
```
 

## 🔹 Etiquetas (Tags)
```bash
git tag                      # Listar tags existentes
git tag v1.0                 # Crear un tag simple
git tag -a v1.0 -m "Versión 1.0"   # Crear tag anotado con mensaje
git show v1.0                # Ver detalles de un tag
git push origin v1.0         # Subir un tag al remoto
git push origin --tags       # Subir todos los tags
```
 

## 🔹 Colaboración y resolución de conflictos
Cuando varias personas trabajan en el mismo archivo, pueden ocurrir conflictos.
Estos comandos ayudan a resolverlos:
```bash
git pull --rebase            # Actualizar rama aplicando commits encima de los nuevos
git merge nombre-rama        # Fusionar otra rama a la actual
```
 
 Si hay conflicto:
 1. Editar manualmente los archivos
 2. Marcar como resuelto
```bash
git add archivo_conflicto.txt
git commit                   # Confirmar resolución
```
 

## 🔹 Recuperar commits y ramas borradas
```bash
git reflog                   # Ver todas las referencias (incluyendo commits borrados)
git checkout <id-commit>     # Volver a un commit específico
git branch recuperar <id>    # Crear una nueva rama a partir de un commit perdido
```



