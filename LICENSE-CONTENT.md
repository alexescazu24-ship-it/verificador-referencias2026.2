# Licencia del contenido editorial · Editorial content license

Bibliochecker se distribuye con **dos licencias**, porque el código y el contenido
editorial conviven en un mismo archivo:

| Parte | Licencia | Archivo |
|---|---|---|
| Código | GNU Affero General Public License v3.0 o posterior | [`LICENSE`](LICENSE) |
| Contenido editorial | Creative Commons Atribución 4.0 Internacional | este archivo |

---

## Dónde está el límite

Todo está en `index.html`, así que conviene decir con precisión qué es cada cosa.

**Es código, y se rige por la AGPL-3.0-or-later:**

- La estructura HTML y las hojas de estilo.
- Todo el JavaScript: el análisis de referencias, las expresiones regulares, las
  consultas a CrossRef, Semantic Scholar, OpenAlex, PubMed y DataCite, el cálculo del
  estado de cada referencia, el algoritmo de similitud y las funciones de exportación.
- Los umbrales y reglas de decisión, aunque se expresen como texto.

**Es contenido editorial, y se rige por la CC BY 4.0:**

- Los textos de la interfaz: los mensajes de resultado, las observaciones, los avisos y
  las etiquetas, en español, inglés y portugués (el objeto `LANGS`).
- El manual de usuario completo, sus ocho secciones en los tres idiomas.
- El texto de «Acerca de» y las notas metodológicas del pie.
- La redacción de los informes que la herramienta exporta.

**No está cubierto por ninguna de las dos:**

- El **logotipo** de Bibliochecker y el nombre de la herramienta. Son identidad visual, no
  documentación: quedan reservados. Se puede reproducir el logotipo para referirse a la
  herramienta, no para identificar una versión modificada o un producto distinto.
- Los datos que devuelven CrossRef, Semantic Scholar, OpenAlex, PubMed y DataCite, que
  pertenecen a cada fuente y se rigen por sus propias condiciones. Bibliochecker no los
  almacena ni los redistribuye: los consulta en el momento y los muestra.

En caso de duda sobre una porción concreta, se aplica la AGPL, que es la más protectora
para quien recibe el programa.

---

## Cómo atribuir el contenido

La CC BY 4.0 solo pide reconocer la autoría. Basta con una línea como esta:

> Textos tomados de Bibliochecker, de Alexander Chinchilla Serrano (Vicerrectoría de
> Investigación, Universidad Estatal a Distancia, Costa Rica), bajo licencia CC BY 4.0.
> https://github.com/alexescazu24-ship-it/verificador-referencias2026.2

Si los modificás, indicá que lo hiciste. No hace falta pedir permiso, ni para uso
comercial.

Texto completo de la licencia: https://creativecommons.org/licenses/by/4.0/deed.es

---

## English summary

Bibliochecker is dual-licensed. The **code** — HTML, CSS and all JavaScript, including the
parsing logic, the API queries, the status thresholds and the export functions — is under
the **GNU AGPL v3.0 or later** (see [`LICENSE`](LICENSE)). The **editorial content** — all
interface strings in Spanish, English and Portuguese, the full user manual, the "About"
text and the wording of the exported reports — is under **Creative Commons Attribution 4.0
International (CC BY 4.0)**.

The Bibliochecker **logo and name are reserved** and covered by neither licence. Data
returned by CrossRef, Semantic Scholar, OpenAlex, PubMed and DataCite belongs to those
sources and follows their own terms; Bibliochecker queries it live and never stores or
redistributes it.

Where it is unclear which part a fragment belongs to, the AGPL applies.

To reuse the content, credit: *Bibliochecker, by Alexander Chinchilla Serrano (Vice-Rectory
for Research, Universidad Estatal a Distancia, Costa Rica), CC BY 4.0* and link back to the
repository. Full licence: https://creativecommons.org/licenses/by/4.0/

---

SPDX-FileCopyrightText: 2026 Alexander Chinchilla Serrano
SPDX-License-Identifier: CC-BY-4.0
