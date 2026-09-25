# Registro de cambios

Formato basado en [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/).
Versionado según [SemVer](https://semver.org/lang/es/).

*An English overview of the tool is available in the [README](README.md).*

---

## [1.0.0] — 2026-09-24

Primera versión documentada y archivada. La herramienta venía publicándose desde junio de
2026 sin registro de cambios: cada actualización era un «Update index.html». Esta entrada
recoge el estado en que queda y los cambios de las últimas semanas, que son los que
alteraron resultados.

### Fuentes de verificación

- **CrossRef** valida el DOI y compara título, autor, año y volumen.
- **DataCite** cubre DOIs de conjuntos de datos, tesis y repositorios, que CrossRef no
  registra. Antes, un DOI de Zenodo o de un repositorio universitario se marcaba como
  problema; era un falso positivo.
- **PubMed**, vía NCBI, aporta cobertura biomédica y la marca «Retracted Publication».
  Se eligió frente a Europe PMC porque esta última no permite consultas desde el navegador.
- **Semantic Scholar** y **OpenAlex** buscan por título. Solo confirman: no encontrar una
  referencia en ellas no la penaliza.
- Enlaces de verificación manual a **Google Scholar**, **PubPeer** y **Retraction Watch**.

### Estados

Cinco: Válida, Sospechosa, Problema, Sin DOI y Retractado. Un DOI y un título confirmados
por CrossRef o DataCite ya no pueden ser rebajados por los buscadores que trabajan por
título, cuyo primer resultado suele ser otro artículo.

### Corregido

- **Referencias fusionadas.** El separador no reconocía fechas como `(2019, 28 de julio)`
  ni `(s.f.)`, y partía las listas largas de autores por la mitad. Una referencia fusionada
  con otra quedaba sin verificar, que es el fallo más grave posible en esta herramienta.
- **Títulos no detectados.** El texto copiado de PDF o Word trae saltos de línea a mitad de
  referencia; el analizador no los cruzaba. En un documento de 117 referencias, 93 salían
  como «sin título ni DOI» teniéndolo.
- **Cursivas ignoradas.** Las marcas internas de cursiva se habían perdido en una edición
  anterior, de modo que toda la validación de cursivas nunca llegaba a ejecutarse.
- **Apellidos compuestos.** «Sánchez Vignau» se comparaba solo como «Sánchez», y los
  índices suelen guardar «B. Vignau»: daba «autor diferente» siendo correcto. Tampoco
  funcionaba con partículas («de la Vega», «van Groenigen»).
- **Volumen en cursiva.** Se avisaba de que faltaba aunque estuviera, cuando la cursiva
  abarcaba también el número de ejemplar.
- **Años falsamente incorrectos.** CrossRef guarda la fecha de publicación en línea y APA
  cita el año del volumen impreso; se comparaba contra la primera.
- **Fechas y autores de páginas web.** `(2019, 28 de julio)`, `(s.f.)` y los autores
  institucionales son válidos en APA 7 y se marcaban como error de formato.
- **DOIs con el dominio antiguo** `dx.doi.org`, frecuentes en revistas latinoamericanas,
  no se reconocían.
- **Retractaciones que no se detectaban.** Se leía el campo de CrossRef que significa
  «este registro *es* un aviso de retractación» en lugar del que significa «a este artículo
  *lo* retractaron», que es el que trae los datos de Retraction Watch. Por eso se escapaban
  casos tan conocidos como Wakefield (1998) o el artículo de Surgisphere en el *New England
  Journal of Medicine*. Se añadió además la lectura de la marca «RETRACTED» en el título
  registrado: sobre 40 artículos retractados, 12 no tienen ningún metadato y solo se
  delatan así.
- **Licencia.** El archivo `LICENSE` contenía la GPL-3.0 y no la AGPL-3.0 que la
  herramienta declara.

### Cambiado

- Las observaciones se generan en un solo lugar y son iguales en pantalla y en los informes
  exportados. Solo se muestra lo que explica el estado de la referencia, no cada fuente que
  no la encontró.
- Las referencias sin DOI reciben **una sola explicación**, siempre la misma, que enumera
  los casos en que es normal no tenerlo.
- Interfaz y manual en **español, inglés y portugués**.
- La referencia se muestra completa, sin recortes, y el botón de copiar es un icono.

---

## Limitaciones conocidas

Se documentan porque la herramienta sirve para revisar integridad y conviene saber dónde
no alcanza.

- **Sin DOI no hay verificación automática de existencia.** La herramienta puede revisar el
  formato y sugerir dónde buscar, nada más.
- **Semantic Scholar y OpenAlex limitan las consultas** sin clave. Cuando no responden, la
  herramienta continúa con las demás fuentes, pero dos análisis del mismo documento pueden
  no coincidir. Un informe sin problemas puede significar que las fuentes no contestaron.
- **La detección de retractaciones no es exhaustiva.** Se revisan cuatro señales —el dato
  de retractación de CrossRef, el aviso, la marca «RETRACTED» en el título y la marca de
  PubMed—, pero si la editorial no depositó nada ni marcó el título, la retractación no
  aparece. Por eso están los enlaces manuales a PubPeer y Retraction Watch.
- **PubMed solo cubre lo biomédico.**
- **El separador de referencias funciona mejor con una línea en blanco entre cada una.**
  Pegadas sin separación, algunas pueden fusionarse. La herramienta muestra cuántas detectó
  y pide comprobar que coincidan con el total real.
- **Las cursivas solo se revisan** si el texto se pega desde Word o se carga un `.docx`.
- **Un resultado «Válida» no garantiza nada.** Las bases de datos son incompletas y sus
  metadatos a veces incorrectos. La revisión humana sigue siendo obligatoria.

---

## Anterior a 1.0.0

Publicado desde junio de 2026 sin registro de cambios. La release `v.2`, de junio, conserva
ese estado inicial.
