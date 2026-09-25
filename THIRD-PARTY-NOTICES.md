# Componentes y servicios de terceros · Third-party notices

Bibliochecker es un único archivo HTML sin dependencias empaquetadas: no hay `node_modules`
ni proceso de compilación. Lo que sigue es todo lo que la página carga o consulta desde
fuera, y en qué condiciones.

---

## 1. Biblioteca incluida desde CDN

### JSZip 3.10.1

Se usa para leer archivos `.docx`, que son contenedores ZIP. Se carga desde
`cdnjs.cloudflare.com`.

- Autor: Stuart Knightley y colaboradores — https://github.com/Stuk/jszip
- Licencia: **MIT o GPL-3.0-or-later**, a elección de quien la use. Bibliochecker la usa
  bajo los términos de la **MIT**, que es compatible con la AGPL-3.0 de este proyecto.
- JSZip incorpora **pako**, también bajo licencia MIT
  (https://github.com/nodeca/pako).

---

## 2. Tipografías

La interfaz carga desde `fonts.googleapis.com` y `fonts.gstatic.com`:

| Tipografía | Licencia |
|---|---|
| Space Grotesk | SIL Open Font License 1.1 |
| IBM Plex Sans | SIL Open Font License 1.1 |
| IBM Plex Mono | SIL Open Font License 1.1 |
| Plus Jakarta Sans | SIL Open Font License 1.1 |
| Source Serif 4 | SIL Open Font License 1.1 |

Las cinco son de fuente abierta, pero **se sirven desde servidores de Google**, de modo que
abrir la página comunica la dirección IP del visitante a Google. Quien necesite evitarlo
puede incrustar las tipografías en el propio archivo o sustituirlas por las del sistema:
la licencia de Bibliochecker lo permite sin pedir permiso.

---

## 3. Medición de uso

La página incluye **Google Analytics** (`gtag.js`, identificador `G-W0BLFQSPY7`) para
contar visitas. Implica que Google recibe datos de la visita y puede usar cookies.

**Las referencias que se analizan no pasan por Analytics**, ni por ningún servidor propio:
se procesan en el navegador y solo viajan a las bases bibliográficas que se listan abajo,
para consultarlas.

Quien reutilice este código puede quitar Analytics borrando el bloque `gtag` de la cabecera
de `index.html`; la herramienta funciona igual sin él.

---

## 4. Imagen del distintivo de licencia

El pie muestra el distintivo de Creative Commons servido desde `i.creativecommons.org`.
Marca de Creative Commons, usada para identificar la licencia del contenido.

---

## 5. Bases bibliográficas consultadas

Bibliochecker consulta estas interfaces públicas en el momento del análisis. No requieren
clave, no se almacena ninguna respuesta más allá de la sesión del navegador, y los datos
que devuelven pertenecen a cada fuente y se rigen por sus propias condiciones de uso.

| Fuente | Para qué | Condiciones |
|---|---|---|
| CrossRef | Verificar el DOI y comparar título, autor, año y volumen; detectar retractaciones | https://www.crossref.org/documentation/retrieve-metadata/rest-api/ |
| DataCite | Verificar DOIs de conjuntos de datos, tesis y repositorios | https://support.datacite.org/docs/api |
| Semantic Scholar | Buscar el trabajo por título | https://www.semanticscholar.org/product/api |
| OpenAlex | Buscar el trabajo por título | https://docs.openalex.org/ |
| PubMed (NCBI E-utilities) | Verificar referencias biomédicas y marcas de retractación | https://www.ncbi.nlm.nih.gov/books/NBK25497/ |

Semantic Scholar y OpenAlex limitan las consultas sin clave y pueden dejar de responder
durante un rato. Cuando eso ocurre, Bibliochecker sigue con las demás fuentes y lo refleja
en el resultado.

Los enlaces manuales a **Google Scholar**, **PubPeer** y **Retraction Watch** no consultan
nada: abren el buscador de cada sitio en una pestaña nueva.

---

## English summary

Bibliochecker is a single HTML file with no bundled dependencies. It loads **JSZip 3.10.1**
from a CDN (used under the **MIT** option of its MIT-or-GPLv3 dual licence; it bundles
**pako**, MIT), and five **SIL OFL 1.1** typefaces served from Google's servers, which
exposes the visitor's IP to Google. The page also includes **Google Analytics**
(`G-W0BLFQSPY7`) for visit counting; the references being checked never pass through it and
never reach any server of our own. Analytics can be removed by deleting the `gtag` block in
the head of `index.html`.

Reference data is queried live from **CrossRef, DataCite, Semantic Scholar, OpenAlex** and
**PubMed (NCBI)**; it belongs to those sources and follows their own terms. Links to Google
Scholar, PubPeer and Retraction Watch are plain links and query nothing.
