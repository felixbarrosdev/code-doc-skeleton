# Code Documentation Skeleton
[![Validate Docs](https://github.com/felixbarrosdev/code-doc-skeleton/actions/workflows/validate-docs.yml/badge.svg)](https://github.com/felixbarrosdev/code-doc-skeleton/actions/workflows/validate-docs.yml)

Este repositorio contiene una estructura modular para escribir y publicar documentación técnica.
Se basa en **MkDocs** y está pensado para proyectos que siguen la filosofía *documentation‑first*.

## ¿Para qué sirve?
- Mantener separada la documentación en módulos temáticos.
- Facilitar la colaboración mediante plantillas reutilizables.
- Publicar un sitio estático con GitHub Pages.

## Levantar el sitio local
1. Instalar las dependencias:
   ```bash
   python -m pip install -r requirements.txt
   ```
2. Ejecutar el servidor de MkDocs:
   ```bash
   mkdocs serve
   ```
   El sitio estará disponible en `http://localhost:8000`.

## Publicar en GitHub Pages
1. Genera el sitio estático:
   ```bash
   mkdocs build
   ```
   Los archivos se crean en la carpeta `public/`.
2. Publica el contenido de `public/` en la rama **gh-pages** o habilita GitHub Pages en esa carpeta.

## ¿Qué contiene cada carpeta?
- **docs/**: documentación fuente organizada por temas (flujos de usuarios, reglas de negocio, APIs, etc.).
- **templates/**: archivos base para crear nuevas secciones de documentación.
- **public/**: salida generada por `mkdocs build`; es la que se publica en GitHub Pages.
- **mkdocs.yml**: configuración del sitio y del menú de navegación.

## Cómo usar los templates
1. Copia el archivo deseado de `templates/` a la ubicación apropiada dentro de `docs/`.
   Por ejemplo:
   ```bash
   cp templates/TEMPLATE-api.md docs/apis/nueva-api.md
   ```
2. Rellena los campos del template con la información de tu proyecto.
3. Agrega la nueva página al menú editando `mkdocs.yml` si es necesario.

Con esta estructura podrás mantener tu documentación organizada y lista para publicarse.

## Configurar tu proyecto
1. Edita `mkdocs.yml` para actualizar `site_name` y `repo_url`.
2. Personaliza los colores y características del tema en la sección `theme`.
3. Agrega tus páginas a la clave `nav` para que aparezcan en la navegación.


## Publicar la documentación

Para compilar y publicar el sitio:

```bash
pip install -r requirements.txt
mkdocs gh-deploy --clean
```
