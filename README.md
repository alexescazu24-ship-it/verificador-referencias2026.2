# Bibliochecker

**Verificador de referencias bibliográficas en APA 7, para detectar alucinaciones de IA.**

▶ **Usar la herramienta:** https://alexescazu24-ship-it.github.io/verificador-referencias2026.2/

Se pega la lista de referencias y Bibliochecker las contrasta, una por una, contra bases
bibliográficas reales para señalar las que no existen, las que mezclan datos de trabajos
distintos y las que fueron retractadas. Funciona en el navegador, sin instalar nada y sin
crear ninguna cuenta.

Nació de la práctica editorial en **UNED Research Journal**, de la Vicerrectoría de
Investigación de la Universidad Estatal a Distancia de Costa Rica, ante un problema cada
vez más común: referencias generadas con ayuda de IA que parecen impecables —autores
reales, revistas conocidas, títulos verosímiles— y que al revisarlas no existen.

---

## ⚠️ Revisión humana obligatoria

Bibliochecker es un **apoyo automatizado, no un dictamen**. Orienta la revisión, no la
sustituye. **El único criterio final válido es el del profesional que corrobora cada
referencia directamente en la fuente original.**

Una referencia marcada como válida puede tener errores que ninguna comprobación automática
detecta, y una marcada como sospechosa puede estar perfectamente bien: las bases de datos
son incompletas y sus metadatos, a veces, incorrectos.

---

## Qué comprueba

| Fuente | Qué aporta |
|---|---|
| **CrossRef** | Valida el DOI y compara título, autor, año y volumen. Detecta retractaciones. |
| **DataCite** | Valida DOIs de conjuntos de datos, tesis y repositorios, que CrossRef no registra. |
| **Semantic Scholar** | Busca el trabajo por título. Solo confirma. |
| **OpenAlex** | Busca el trabajo por título. Solo confirma. |
| **PubMed** | Cobertura biomédica. Marca artículos retractados. Solo confirma. |
| **APA 7** | Revisa el formato: fecha, autores, cursivas, DOI en formato de enlace. |

Cada referencia recibe uno de cinco estados: **Válida**, **Sospechosa**, **Problema**,
**Sin DOI** o **Retractado**. Los resultados se exportan a HTML, Word o Excel.

La interfaz y el manual están en **español, inglés y portugués**.

---

## Privacidad

**Las referencias que se analizan no se almacenan ni pasan por ningún servidor propio.** Se
procesan en el navegador y solo viajan a las bases bibliográficas de la tabla anterior, que
es lo que permite verificarlas. No hay cuentas, ni registro, ni envío de correos.

Con transparencia: la página **sí incluye Google Analytics** para contar visitas, y carga
tipografías desde servidores de Google. Ninguno de los dos recibe el texto de las
referencias. Ambos se pueden quitar del archivo; está explicado en
[`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md).

---

## Licencias

Este proyecto tiene **dos licencias**, porque el código y el contenido editorial conviven
en el mismo archivo:

- **Código** — GNU Affero General Public License v3.0 o posterior
  (`AGPL-3.0-or-later`). Ver [`LICENSE`](LICENSE).
- **Contenido editorial** — Creative Commons Atribución 4.0 Internacional (`CC-BY-4.0`):
  textos de interfaz, manual, «Acerca de» y redacción de los informes. Ver
  [`LICENSE-CONTENT.md`](LICENSE-CONTENT.md), que explica **dónde está el límite** entre
  uno y otro.
- El **logotipo y el nombre** quedan reservados y no los cubre ninguna de las dos.

Se eligió la AGPL a propósito: es una herramienta que se usa a través de la red, y la AGPL
obliga a que quien la ofrezca modificada ponga su código a disposición de quien la use. El
enlace al código fuente está en el pie de la propia aplicación.

Componentes y servicios de terceros: [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md).

---

## Cómo citar

Usá el botón **«Cite this repository»** de GitHub, que lee [`CITATION.cff`](CITATION.cff),
o bien:

> Chinchilla Serrano, A. (2026). *Bibliochecker: verificador de referencias bibliográficas
> APA 7* [Software]. Vicerrectoría de Investigación, Universidad Estatal a Distancia.
> https://github.com/alexescazu24-ship-it/verificador-referencias2026.2

---

## Créditos

Creado por **Alexander Chinchilla Serrano** · Vicerrectoría de Investigación, Universidad
Estatal a Distancia (UNED) · San José, Costa Rica · 2026 · fchinchillas@uned.ac.cr

**Codificación:** Claude Code (Anthropic) — identificadores de modelo `claude-opus-5` y
`claude-sonnet-5` — bajo instrucción, criterio y experiencia editorial humana.

---
---

# Bibliochecker (English)

**An APA 7 reference checker built to catch AI hallucinations.**

▶ **Use it:** https://alexescazu24-ship-it.github.io/verificador-referencias2026.2/

Paste a reference list and Bibliochecker checks each entry against real bibliographic
databases, flagging references that do not exist, mix data from different works, or have
been retracted. It runs in the browser: no installation, no account.

It comes out of editorial practice at **UNED Research Journal** (Vice-Rectory for Research,
Universidad Estatal a Distancia, Costa Rica), facing an increasingly common problem:
AI-assisted references that look flawless — real authors, well-known journals, plausible
titles — and turn out not to exist.

### ⚠️ Human review is required

Bibliochecker is **automated support, not a verdict**. It guides review, it does not
replace it. **The only valid final criterion is that of the professional who verifies each
reference directly in the original source.** A "valid" result may still hide errors, and a
"suspicious" one may be perfectly fine: databases are incomplete and their metadata is
sometimes wrong.

### What it checks

**CrossRef** validates the DOI and compares title, author, year and volume, and detects
retractions. **DataCite** covers DOIs for datasets, theses and repositories. **Semantic
Scholar** and **OpenAlex** search by title, confirm-only. **PubMed** covers biomedical work
and flags retracted articles. An **APA 7** pass reviews formatting. Each reference gets one
of five statuses — Valid, Suspicious, Problem, No DOI, Retracted — and results export to
HTML, Word or Excel. Interface and manual in Spanish, English and Portuguese.

### Privacy

**The references you check are never stored and never pass through any server of ours.**
They are processed in the browser and only travel to the bibliographic databases above.
No accounts, no sign-up, no email. In the interest of transparency: the page **does include
Google Analytics** for visit counting and loads fonts from Google's servers. Neither
receives the text of your references. Both can be removed — see
[`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md).

### Licensing

Dual-licensed. **Code** under the **GNU AGPL v3.0 or later** ([`LICENSE`](LICENSE));
**editorial content** — interface strings, manual, "About" text and report wording — under
**CC BY 4.0** ([`LICENSE-CONTENT.md`](LICENSE-CONTENT.md), which sets out exactly where the
boundary lies). The **logo and name are reserved** and covered by neither. The AGPL was a
deliberate choice: this is network-facing software, and the AGPL requires anyone who offers
a modified version to make its source available to its users.

### Credits

Created by **Alexander Chinchilla Serrano** · Vice-Rectory for Research, Universidad Estatal
a Distancia (UNED) · San José, Costa Rica · 2026 · fchinchillas@uned.ac.cr

**Coding:** Claude Code (Anthropic) — model identifiers `claude-opus-5` and
`claude-sonnet-5` — under human editorial instruction, judgement and experience.
