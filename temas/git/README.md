# Git
Git es un software de control de versiones diseñado por Linus Torvalds

## Secciones principales de un proyecto de Git

![Git](https://bit.ly/3pt4oHu)


## Instalación
[Git](https://git-scm.com/downloads) Descargala e instalar.

## Comandos

Lo primero que debe hacer al instalar Git es configurar su nombre de usuario y dirección de correo electrónico.

```java
user@mrcastro/c/git(master)
$ git config --global user.name "Mr Castro"
$ git config --global user.email mrcastro@example.com
```

## Iniciar un Proyecto
```java
user@mrcastro/c/git
git init

user@mrcastro/c/git(master)
$
```

## Añadir cambios
```java
user@mrcastro/c/git(master)
$ git add .
```
## Confirmacion de cambios
```java
user@mrcastro/c/git(master)
$ git commit -m "my first commit"
```
## Visualizar los estados
```java
user@mrcastro/c/git(master)
$ git status
on branch master
```

## Deshacer un git add .
```java
user@mrcastro/c/git(master)
$ git reset
```

## Eliminar un repositorio git
```java
user@mrcastro/c/git(master)
$ rm -rf .git

user@mrcastro/c/git
$
```



## Merge
El comando git merge permite tomar las líneas independientes de desarrollo 

creadas por git branch e integrarlas en una sola rama.

**Solucionar un problema común con Git Merge**

Please enter a commit message to explain why this merge is necessary



```javascript
// si esta usando Vim
1.- Presione "i" (i para insertar)
2.- Escribe tu mensaje de fusión
3.- Presione "esc" (escape)
4.- Escriba ": wq" (escribir y salir)
5.- Luego presione enter

```

