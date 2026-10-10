# Constructor de Estrategias Tau

Herramienta web para construir estrategias de búsqueda sistemática según el marco de la pregunta (PICO, PICOS, PECO, PEO, PIRD, PFO, CoCoPop, PCC, PICo, SPIDER, SPICE y bloque para umbrella review), con sintaxis para PubMed, Scopus, Web of Science, Embase, Cochrane Library, BVS/LILACS y ERIC.

**Autor:** Dr. Joshuan J. Barboza, MD, PhD · Tau Clinical Research · ORCID 0000-0002-2896-1407
**Cursos:** https://investigaciontau.com/cursos-online/

## Archivos
| Archivo | Contenido |
|---|---|
| `index.html` | La aplicación completa (HTML + CSS + JS) |
| `mesh-data.js` | MeSH 2026 (NLM): 31 110 descriptores, términos de entrada no permutados, números de árbol y equivalentes en español (Wikidata, CC0) |
| `scr-data-1.js` … `scr-data-4.js` | 324 046 conceptos suplementarios MeSH 2026 (fármacos, sustancias, enfermedades raras, organismos, protocolos) con sinónimos y descriptores a los que mapean; se cargan en segundo plano |
| `eric-data.js` | ERIC Thesaurus 2025 (IES) completo: 4578 descriptores con nota de alcance, Use For, BT, NT y RT |
| `logo.png` | Logo Tau Clinical Research |

## Publicar en GitHub Pages
1. Crea una carpeta en tu repositorio `jbarbozameca.github.io` (p. ej. `/estrategias/`) y sube todos los archivos del paquete.
2. Haz commit; la herramienta queda en `https://jbarbozameca.github.io/estrategias/`.

## Funciones en vivo (requieren internet, sin clave)
- NCBI E-utilities: conteo de resultados por bloque en PubMed, validación con PMID semilla, notas de alcance y búsqueda de conceptos suplementarios MeSH (fármacos, etc.).
- DeCS oficial (BIREME): opcional, con clave gratuita de api.bvsalud.org introducida en "Opciones".

## Reglas de construcción
- PubMed sin corchetes ni etiquetas de campo; límites desde los filtros.
- Un bloque por variable de la pregunta (+ bloque de diseño en umbrella review).
- Sin truncadores ni comodines.
- Frases compuestas exactas; doble columna (controlado + libre) unida por OR; sin NOT.

## Actualizar MeSH
Descarga `desc20XX.gz` de https://nlmpubs.nlm.nih.gov/projects/mesh/MESH_FILES/xmlmesh/ y regenera `mesh-data.js` con el mismo formato: `[número UI, encabezado, árboles separados por ';', términos de entrada separados por '|' (prefijo ^ = sigla, $ = marca), términos en español separados por '|']`.

## DeCS oficial
El uso de la base DeCS requiere un acuerdo de licencia gratuito con OPS/BIREME (https://forms.office.com/r/Vz3gefsXF6; condiciones en https://decs.bvsalud.org/es/condiciones-para-descargar-los-datos-de-decs-mesh/). Con el XML licenciado se genera `decs-data.js` y se integra igual que los demás vocabularios, citando la edición y los derechos de OPS/BIREME.
