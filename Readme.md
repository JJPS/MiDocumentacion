# Cómo publicar documentación generada con MkDocs en GitHub Pages

## Requisitos

- Tener instalado [MkDocs](https://www.mkdocs.org/) 
- Tener instalado [GIT](https://git-scm.com/)
- Tener cuenta en [GitHUB](https://github.com/)

## Crear repositorio en GitHUB

Accedemos a nuestra cuenta de GitHUB y creamos un repositoro vacío.

![RepositorioGitHUB](./imagenes/repositorioGitHub.jpg)

## Crear repositorio MkDocs

Desde la consola creamos el repositorio MkDocs, y accedemos a él.

```BASH
mkdocs new MiDocumentacion
cd MiDocumentacion
```

## Hacer PUSH de GitHUB en carpeta de MkDocs

Desde la consola y dentro del repositorio que acabamos de crear:

```BASH
git init
git add .
git commit -m "Commit inicial"
git remote add origin https://github.com/JJPS/MiDocumentacion.git
git branch -M main
git push -u origin main
```

## Crear documentación

Con nuestro editor favorito creamos la documentación usando la siguiente [Guía de Uso](https://www.mkdocs.org/getting-started/)

## Desplegar documentación

Desde consola y dentro del repositorio donde tenemos la documentación:

```BASH
mkdocs gh-deploy
```

Este comando generará nuestra página estática y mostrará en qué URL está disponible. La activación de la WEB no es inmediata y tarda unos minutos en estar disponible.

## Actualizar repositorio GIT

El desplegar la documentación no conlleva la actualización del contenido de nuestra página en GIT. Por lo que debermos sincronizar los contenidos entre nuestro equipo y GitHUB

```BASH
git add .
git -m commit "Actualización ..."
git push
```



