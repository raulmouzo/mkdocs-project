# Versionado

Material for MkDocs permite facilmente crear y desplegar versiones de nuestra documentación. De esta manera podremos desplegar nuevas versiones sin modificar las anteriores y dejandolas disponibles para el público.

En nuestro caso usaremos [mike](https://github.com/jimporter/mike) que nos permite ...mike is a Python utility that makes it easy to deploy multiple versions of your MkDocs-powered docs to a Git branch, suitable for hosting on Github via gh-pages. To see an example of this in action, take a look at the documentation for bfg9000.


## Activar versionado con `mike`

Para activar en versionado con mike debemos añadir lo siguiente a nuestro archivo de configuración `mkdocs.yml`:

```yaml
extra:
  version:
    provider: mike
```

!!! note "Condiciones para mantener al usuario en la misma página al cambiar de versión"
    - [site_url] debe estar configurada correctamente en mkdocs.yml.
    - Debes estar visualizando el sitio en esa URL (y no localmente, por ejemplo).
    - La redirección ocurre mediante JavaScript y no hay forma de saber a qué página serás redirigido con anticipación.

## Cómo usar `mike` para desplegar versiones

### Publicar una nueva versión

```bash
mike deploy --push --update-aliases 1.0 latest
```
- **`mike deploy`**: desplegar versiones de la documentación.

- **`--push`**: envía los cambios al repositorio remoto (necesario si usamos `gh-pages`, por ejemplo).

- **`--update-aliases`**: indica que si ya existe un alias (en este caso, `latest`), se debe actualizar para apuntar a la nueva versión (`1.0`). 

- **`1.0`**: versión a desplegar.

- **`latest`**: alias que se asigna a la versión desplegada. 


### Establecer una versión como predeterminada

Si usamos versionado debemos tener una versión predeterminada que se muestra al usuario al entrar a la web y que se irá actualizando según se actualicen la documentación.

Comúnmente se usa el alias `latest`.

```bash
mike set-default --push latest
```


### Otros los comandos de `mike`:

* Despliegue de versión: `mike deploy [versión]`
* Desplegar documentación: `mike deploy [versión] [alias]...`
* Desplegar en local: `mike serve`
* Borrar documentos: `mike delete [identificador]...`
* Listado de documentos: `mike list`
* Establecer versión predeterminada: `mike set-default [identificador]`
* Cambiar título de una versión: `mike retitle [identificador] [título]`
* Agregar alias a una versión: `mike alias [identificador] [alias]...`
* Gestión de propiedades: `mike props [identificador] [propiedad]`

Para más información consultar mike en [Github](https://github.com/jimporter/mike/tree/master).




## Advertencia en versión desactualizada

Cuando el usuario se encuentra en una versión desactualizada de la documentación, puede ser útil mostrar una pequeña advertencia en la parte superior de la pantalla para informar sobre este estado.

En MkDocs, esta funcionalidad se puede lograr mediante el uso de la **extensión de tema**, que permite sobrescribir ciertas partes de la interfaz.

#### Activación de la extensión de tema

Para habilitar esta función, debemos agregar lo siguiente a nuestro archivo de configuración `mkdocs.yml`:

```yaml
theme:
  name: material
  custom_dir: overrides
```

En esta sección, explicamos cómo activar la extensión de tema para este caso específico. Puedes encontrar información adicional [aquí](https://squidfunk.github.io/mkdocs-material/customization/#extending-the-theme).

### Configuración de la Advertencia

Para agregar la advertencia, crea un archivo llamado `main.html` en la carpeta "overrides" con el siguiente contenido:

```html
{% extends "base.html" %}

{% block outdated %}
  Estás utilizando una versión desactualizada.
  <a href="{{ '../' ~ base_url }}"> 
    <strong>Haz clic aquí para acceder a la última versión.</strong>
  </a>
{% endblock %}
```
!!! info
    Este código personalizado mostrará un mensaje indicando que la versión está desactualizada, junto con un enlace para acceder a la última versión.