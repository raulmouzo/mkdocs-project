# Búsqueda

Material for MkDocs nos facilita la integración de una barra de búsqueda de manera sencilla, incluso posibilitando la búsqueda sin conexión.

El plugin de búsqueda integrado se integra perfectamente con Material for MkDocs, proporcionando búsqueda multilingüe. 

Está habilitado por defecto, pero **debe volverse a agregar a `mkdocs.yml` cuando se utilizan otros plugins**:

```yaml
plugins:
  - search
```

## Sugerencias de Búsqueda:

Cuando activas las sugerencias de búsqueda, esta presentará la posible completación para la última palabra, la cual puedes aceptar con la tecla derecha. 

Añade las siguientes líneas a tu archivo mkdocs.yml:

```yaml
theme:
  features:
    - search.suggest
```

## Resaltado de Búsqueda:
Puedes configurar la búsqueda para resaltar todas las coincidencias de la siguiente manera:
```yaml
theme:
  features:
    - search.highlight
```
!!! info
    Para ver todas las configuraciones, consulta la [documentación del plugin](https://squidfunk.github.io/mkdocs-material/plugins/search/).
