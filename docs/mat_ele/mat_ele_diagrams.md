# Diagramas

Material for MkDocs ofrece integración con **Mermaid.js**, permitiendo incorporar diversos tipos de diagramas a tu documentación de proyecto. Aquí te presentamos cómo configurar y utilizar algunos de ellos.

## Configuración:

Para configurar los diagramas añadiremos lo siguiente a `mkdocs.yml`:

```yaml
markdown_extensions:
  - pymdownx.superfences:
      custom_fences:
        - name: mermaid
          class: mermaid
          format: !!python/name:pymdownx.superfences.fence_code_format
```

## Uso de diagramas

````markdown title="Diagrama de flujo"
```mermaid 
graph LR
  A[Inicio] --> B{¿Estudiante de la UDC?};
  B -->|Sí| C[Inscribirse en clases];
  C --> D[Estudiar];
  D --> B;
  B ---->|No| E[¡Finalizar estudios!];
```
````
<div class="result" markdown>

```mermaid 
graph LR
  A[Inicio] --> B{¿Estudiante de la UDC?};
  B -->|Sí| C[Inscribirse en clases];
  C --> D[Estudiar];
  D --> B;
  B ---->|No| E[¡Finalizar estudios!];
```
</div>

````markdown title="Diagrama entidad-relación"
```mermaid 
graph TD
  A[Inicio] -->|Solicitar admisión| B[Proceso de Admisión]
  B -->|Aprobado| C[Matricularse]
  B -->|Rechazado| D[Fin del Proceso]
  C --> E{¿Asignaturas Disponibles?}
  E -->|Sí| F[Seleccionar Asignaturas]
  E -->|No| D[Fin del Proceso]
  F --> G[Inicio de Clases]
  G --> H{¿Éxito Académico?}
  H -->|Sí| I[Continuar Estudios]
  H -->|No| D[Fin del Proceso]
  I --> D[Fin del Proceso]

```
````

<div class="result" markdown>

```mermaid 
graph TD
  A[Inicio] -->|Solicitar admisión| B[Proceso de Admisión]
  B -->|Aprobado| C[Matricularse]
  B -->|Rechazado| D[Fin del Proceso]
  C --> E{¿Asignaturas Disponibles?}
  E -->|Sí| F[Seleccionar Asignaturas]
  E -->|No| D[Fin del Proceso]
  F --> G[Inicio de Clases]
  G --> H{¿Éxito Académico?}
  H -->|Sí| I[Continuar Estudios]
  H -->|No| D[Fin del Proceso]
  I --> D[Fin del Proceso]
```
</div>

Existen más tipos de diagramas como secuencia, estado y clase. Para detalles adicionales y ejemplos, consulta la documentación de Mermaid.js [aquí](http://mermaid.js.org).


