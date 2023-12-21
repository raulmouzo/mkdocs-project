# Importar Documentación

## Añadir Nuevas Páginas

Una vez que hayas configurado los parámetros esenciales de la página, el siguiente paso es incorporar tu documentación. Para ello, utiliza el elemento `nav`. En el contexto de MkDocs, `nav` es un componente esencial que te permite definir la estructura de navegación, especificando enlaces y disposición de páginas.

Para agregar nuevas páginas de documentación, créalas primero en el directorio `docs` y luego agrégales siguiendo el formato: `- Nombre: archivo.md`. Se añadirán automáticamente a la barra de navegación.

> Ejemplo de configuración

```yaml
nav: 
  - Home: index.md
  - 'Page 1': 'p1.md'
  - 'Page 2': 'p2.md'
  - 'Page 3': 'p3.md'
```

![Imagen de navegación](img/img_nav.png)

Observa que se añade automáticamente una barra de búsqueda (que configuraremos más adelante) y un enlace directo al repositorio de GitHub especificado anteriormente.

