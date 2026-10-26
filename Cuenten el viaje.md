# 🚀 Cuenten el viaje:  (Práctica 6)

## 1. El flujo de trabajo 
- **Estructura de ramas:** Utilizamos `main` como la rama de producción con la versión estable y publicada. La rama `develop` sirvió como la línea base de integración para centralizar todo el trabajo en desarrollo. Las ramas `feature/aurora-lanzamiento` y `feature/orbita-aterrizaje` se utilizaron para trabajar de forma aislada en las tareas específicas de cada misión sin afectar el código base.
- **Creación y subida de ramas:** Cada equipo creó su rama de características partiendo del estado inicial de `develop` mediante `git switch -c feature/... origin/develop`. Realizamos las modificaciones en las misiones y en `panel/estado.md`, confirmamos los cambios con `git commit` y publicamos las ramas remotamente mediante `git push -u origin feature/...`. Posteriormente, se abrieron los Pull Requests hacia `develop`.

## 2. Revisión cruzada y resolución de conflictos
- **Revisión de PRs:** Revisamos los cambios de los compañeros a través de la pestaña *Files changed* de GitHub.
- **Resolución de conflictos:** Al integrar la primera misión (Aurora) en `develop`, la segunda misión (Órbita) generó un conflicto en `panel/estado.md`. Sincronizamos la rama ejecutando `git merge origin/develop`, identificamos los marcadores de conflicto (`<<<<<<<`, `=======`, `>>>>>>>`), negociamos el texto de consenso unificado y guardamos los cambios para completar la fusión.

## 3. Publicación final a producción
- **Integración en `main`:** Una vez integradas ambas misiones en `develop`, abrimos el Pull Request final hacia `main`. Tras validar el contenido, realizamos el merge a `main` y actualizamos el entorno local ejecutando `git pull origin main`.

## 4. Comandos clave utilizados
1. `git switch -c <rama> origin/develop`: Para crear y cambiar a una rama de características partiendo de `develop`.
2. `git status`: Para verificar el estado de los archivos y cambios antes de hacer commit.
3. `git pull origin main`: Para sincronizar y descargar en local los cambios finales fusionados en GitHub.
