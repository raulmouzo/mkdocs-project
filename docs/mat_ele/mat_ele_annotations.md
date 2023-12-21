# Anotaciones en código

Una anotación es una aclaración en forma de ventana flotante que se puede implementar en el código.


Por ejemplo, esto es una **anotación** (1)
{ .annotate }

1. 🙋🏻 !Hola! Soy una **anotación** y puedo mostrar cualquier cosa escrita en markdown.



## Configuración

Para implementar esta funcionalidad debemos añadir lo siguiente al archivo de configuración `mkdocs.yml`:

```yaml
markdown_extensions:
  - attr_list
  - md_in_html
  - pymdownx.superfences
```

### Iconos

Se permite el uso de iconos personalizados, que se especifican en el archivo de configuración:

```yaml
theme:
  icon:
    annotation: material/arrow-right-circle
```

## Usos

### En texto

Lorem ipsum dolor sit amet, (1) consectetur adipiscing elit.
{ .annotate }

1. Esta es una anotación en texto.

``` markdown title="Texto con anotaciones"
Lorem ipsum dolor sit amet, (1) consectetur adipiscing elit.
{ .annotate }

1.  Cillum elit nulla non amet excepteur labore non mollit proident cupidatat Lorem sint minim.
```


### En código

### En admonitions

!!! note annotate "Phasellus posuere in sem ut cursus (1)"

    Lorem ipsum dolor sit amet, (2) consectetur adipiscing elit. Nulla et
    euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo
    purus auctor massa, nec semper lorem quam in massa.

1. Esta es una anotación en el encabezado de un admonition.
2. Esta es una anotación en el cuerpo de un admonition.
