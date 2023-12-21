# Pestañas de contenido

Las Material for MkDocs permite agrupar contenido alternativo en pestañas, facilitando la presentación de información sobre el acceso a una API desde diferentes lenguajes o entornos.  de contenido permiten mostrar cierta in

Por ejemplo, para mostrar una implementación a un código en varios lenguajes:

!!! example "Ejemplo"
    === "Python"
        ```python
        def saludar():
            print("¡Hola desde Python!")

        saludar()
        ```
    === "C"
        ```c
        #include <stdio.h>

        void saludar() {
            printf("¡Hola desde C!\n");
        }

        int main() {
            saludar();
            return 0;
        }
        ```
    === "C++"
        ```c++
        #include <iostream>

        void saludar() {
            std::cout << "¡Hola desde C++!" << std::endl;
        }

        int main() {
            saludar();
            return 0;
        }
        ```


## Configuración

Para implementar esta característica, agrega las siguientes líneas al archivo `mkdocs.yml`:

```yaml
theme:
  features:
    - content.tabs.link
```
