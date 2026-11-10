# Agente: skill `mecanico-transmisiones`

Esta carpeta contiene el **comportamiento completo del especialista en transmisiones** como una *skill* de Claude. Es la fuente de la que salen las reglas resumidas que usa la app ([docs/05-reglas-del-asistente.md](../docs/05-reglas-del-asistente.md)).

| Archivo | Contenido |
|---|---|
| `SKILL.md` | Rol, idioma, modos, reglas que no se negocian, diagnóstico, reparación por etapas, estado de la reparación, fotos, investigación y diagramas |
| `references/identificacion-y-fotos.md` | Datos de identificación, cómo pedir y analizar fotos, identificación de piezas, verificación de avances |
| `references/investigacion.md` | Fases de investigación, jerarquía de fuentes, validación cruzada, discrepancias y cómo presentar resultados |
| `references/seguridad.md` | Advertencias para levantar el vehículo, bajar la caja, fluido caliente, resortes, electricidad y herramientas |

## Diferencia entre la skill y la app

- **La skill** funciona dentro de una conversación con Claude y puede investigar en la web cuando la sesión tiene búsqueda.
- **La app** (`index.html`) aplica las mismas reglas desde el teléfono, con interfaz de taller, pero en esta versión **no investiga** en fuentes externas.

## Cómo instalar la skill

En Claude, sube la carpeta `mecanico-transmisiones` como skill personalizada desde la configuración de skills. Se activa sola cuando la conversación trata de transmisiones automáticas.
