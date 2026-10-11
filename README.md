# Constructor de Estrategias Tau

Herramienta web para construir estrategias de búsqueda sistemática en **ciencias de la salud, educación, ciencias sociales, humanidades, derecho e ingenierías**. El usuario elige su área, el marco de la pregunta (PICO, PICOS, PECO, PEO, PIRD, PFO, CoCoPop, PCC, PICo, SPIDER, SPICE, PICOC, ECLIPSE, PNJ y bloque para umbrella review) y obtiene la sintaxis para 16 bases de datos.

**Autor:** Dr. Joshuan J. Barboza, MD, PhD · Tau Clinical Research · ORCID 0000-0002-2896-1407
**Cursos:** https://investigaciontau.com/cursos-online/

## Tesauros incluidos (1 007 411 conceptos)
| Archivo | Tesauro | Conceptos | Licencia |
|---|---|---|---|
| `mesh-data.js` | MeSH 2026 (NLM) + equivalentes en español de Wikidata | 31 110 | Dominio público / CC0 |
| `scr-data-1..4.js` | Conceptos suplementarios MeSH 2026 | 324 046 | Dominio público |
| `voc/ncit-1..5.js` | NCI Thesaurus | 204 721 | CC BY 4.0 |
| `voc/hpo-1.js` | Human Phenotype Ontology | 19 894 | Uso libre con atribución |
| `eric-data.js` | ERIC Thesaurus 2025 (IES) | 4578 | Dominio público |
| `voc/unesco-1.js` | Tesauro de la UNESCO (es/en) | 4500 | CC BY-SA 3.0 IGO |
| `voc/elsst-1.js` | ELSST, CESSDA (es/en) | 3422 | Ver elsst.cessda.eu |
| `voc/eurovoc-1.js` | EuroVoc, Unión Europea (es/en) | 7515 | CC BY 4.0 |
| `voc/stw-1.js` | STW Thesaurus for Economics, ZBW | 6696 | CC BY 4.0 |
| `voc/agrovoc-1.js` | AGROVOC, FAO (es/en) | 42 053 | CC BY 4.0 |
| `voc/gemet-1.js` | GEMET, Agencia Europea de Medio Ambiente (es/en) | 5573 | Reutilización con atribución |
| `voc/nasa-1.js` | NASA Thesaurus | 22 622 | Dominio público |
| `voc/aat-1..2.js` | Getty Art & Architecture Thesaurus (es/en) | 55 575 | ODC-By 1.0 |
| `voc/lcsh-1..4.js` | Library of Congress Subject Headings (sin subdivisiones) | 275 106 | Dominio público |

Los tesauros se cargan solo cuando el usuario activa el área correspondiente.

## Áreas → tesauros y bases
| Área | Tesauros | Bases de datos |
|---|---|---|
| Ciencias de la salud | MeSH, SCR, NCIt, HPO | PubMed, Embase, Cochrane, BVS/LILACS, CINAHL, APA PsycInfo, Scopus, WoS, SciELO |
| Educación | ERIC, UNESCO, MeSH | ERIC, APA PsycInfo, Scopus, WoS, SciELO, Redalyc, Dialnet |
| Ciencias sociales | ELSST, UNESCO, EuroVoc, STW | APA PsycInfo, Scopus, WoS, SciELO, Redalyc, Dialnet, JSTOR |
| Humanidades | UNESCO, AAT, LCSH | JSTOR, Scopus, WoS, Dialnet, SciELO, Redalyc |
| Derecho | EuroVoc, LCSH | HeinOnline, Dialnet, Scopus, WoS, SciELO, Redalyc |
| Ingenierías | NASA, AGROVOC, GEMET, LCSH | IEEE Xplore, ScienceDirect, Scopus, WoS, SciELO |

## Publicar en GitHub Pages
Sube **todo el contenido** del paquete (incluida la carpeta `voc/`) a una carpeta de `jbarbozameca.github.io`, por ejemplo `/estrategias/`. Ningún archivo supera los 9 MB, por debajo del límite de 100 MB de GitHub.

## Reglas de construcción
- PubMed sin corchetes ni etiquetas de campo; límites desde los filtros.
- Un bloque por variable de la pregunta (+ bloque de diseño en umbrella review).
- Sin truncadores ni comodines.
- Frases compuestas exactas; doble columna (controlado + libre) unida por OR; sin NOT.

## DeCS oficial
Requiere el acuerdo de licencia gratuito de OPS/BIREME (https://forms.office.com/r/Vz3gefsXF6). Con el XML licenciado se genera `voc/decs-1.js` en el mismo formato.

## Formato de `voc/*.js`
`[id, término en inglés, término en español, sinónimos EN '|', sinónimos ES '|', términos amplios '|', términos específicos '|', nota]`
