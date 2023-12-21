# Bloques de Código en Material for MkDocs

Los bloques de códigos son muy importantes si queremos representar de forma correcta código de algún lenguaje de programación. Material nos permite configurar esto mediante markdown pero añadiendo nuevas funcionalidades como admoniciones, botones de código, anotaciones, resaltado avanzado, emojis, incrustación de contenido externo y tablas de datos para facilitar la creación de documentación técnica más rica y legible.

## Configuración

La configuración posibilita la activación del resaltado de sintaxis en bloques de código y en línea, así como la inclusión directa de código fuente desde otros archivos. Añade las líneas siguientes a tu archivo `mkdocs.yml`:

```yaml
markdown_extensions:
  - pymdownx.highlight:
      anchor_linenums: true
      line_spans: __span
      pygments_lang_class: true
  - pymdownx.inlinehilite
  - pymdownx.snippets
  - pymdownx.superfences
```

## Funcionalidades adicionales

### Botón para Copiar Código
```yaml
theme:
    features:
    - content.code.copy
```

### Botón para Seleccionar Código
```yaml
theme:
    features:
    - content.code.select
```

### Anotaciones en Código
```yaml
theme:
    features:
    - content.code.annotate
```

### Selectores Personalizados
```yaml
extra:
    annotate:
    json: [.s2]
```

Puedes consultar el total de funcionalidades [aquí](https://squidfunk.github.io/mkdocs-material/reference/code-blocks/).



