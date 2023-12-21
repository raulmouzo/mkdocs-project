# Configuración Básica de MkDocs

MKDocs simplifica la creación de documentación de proyectos mediante Markdown, generando sitios web estáticos para una distribución y mantenimiento sencillos.

Para obtener detalles, consulta: [Getting Started with MkDocs](https://www.mkdocs.org/getting-started/)

## Instalación de MkDocs

En la mayoría de los sistemas, Python suele estar instalado por defecto. Puedes verificarlo con los siguientes comandos:

```bash
python --version
pip --version
```

Si no está instalado, encuentra los instaladores para Windows, Linux y macOS en [Download Python](https://www.python.org/downloads/)

Una vez instalado, procedemos a instalar MkDocs desde pip:

```bash
pip install mkdocs
```

Confirma la instalación de MkDocs con:

```bash
mkdocs --version
```


## Crear un Nuevo Proyecto

Para iniciar un nuevo proyecto, utiliza el siguiente comando:

```bash
mkdocs new nuevo-proyecto
```

Este comando generará un archivo de configuración llamado `mkdocs.yml` y un directorio `docs` que albergará la documentación que planeas presentar en la página.

Con el comando `mkdocs serve`, podrás desplegar la página localmente (http://127.0.0.1:8000/).

## Configuración Básica de `mkdocs.yml`

1. **site_name:** Define el nombre del sitio o la documentación generada.
2. **repo_url:** Especifica la URL del repositorio de código fuente asociado con la documentación (en este ejemplo, Github Pages, pero puede ser otro).
3. **site_description:** Proporciona una breve descripción o resumen del propósito de la documentación o del sitio.
4. **site_author:** Indica el nombre del autor o autores de la documentación.
5. **copyright:** Define la información de derechos de autor para la documentación generada.

> Ejemplo de configuración

```yaml
site_name: MkDocs documentation
repo_url: https://github.com/username/mkdocs-documentation/
site_description: MkDocs documentation website.
site_author: Name Lastname
copyright: 2023 Universidad de La Coruña. Todos los derechos reservados.
```