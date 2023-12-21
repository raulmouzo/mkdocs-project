
# Colores

## Paleta de Colores

- **Esquema de Colores:** define el esquema de colores para el tema.
    - `default` (modo claro)
    - `slate` (modo oscuro)

    ```yaml
    theme:
        palette:
        scheme: default
    ```

- **Color Primario:** establece el color principal para encabezados y componentes.
  ```yaml
  theme:
    palette:
      primary: indigo
  ```
- **Color de Secundario:** define el color para elementos interactivos como enlaces y botones.
  ```yaml
  theme:
    palette:
      accent: indigo
  ```
!!! info ""
    **Colores disponibles:** `red` `pink` `purple` `deep_purple` `indigo` `blue` `light_blue` `cyan` `teal` `green` `light_green` `lime` `yellow` `amber` `orange` `deep_orange`

## Alternar Paleta de Colores (switch odo claro/oscuro)

- **Agregar al mkdocs.yml:**
  Proporciona un switch en la barra superior para cambiar entre modos claro y oscuro.
  ```yaml
  theme:
    palette: 
      - scheme: default
        toggle:
          icon: material/brightness-7 
          name: Modo oscuro
      - scheme: slate
        toggle:
          icon: material/brightness-4
          name: Modo claro
  ```

!!! info 
    También es posible configurar Material for MkDocs para que se ajuste automáticamente a las preferencias de apariencia (clara u oscura) del sistema del usuario. 
    [Más información](https://squidfunk.github.io/mkdocs-material/setup/changing-the-colors/#system-preference)