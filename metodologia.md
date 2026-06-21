# Metodología — razonamiento clínico adversarial y protocolo de búsqueda

> Cómo se construye y se defiende este caso: la persona clínica, el bucle de razonamiento, el protocolo de búsqueda de literatura (APIs) y las reglas anti-alucinación. Es la **fuente de las reglas** del proyecto.

## Contexto

Este proyecto resuelve y prepara la **defensa** de un caso clínico real del **Hospital General Universitario Gregorio Marañón**. El objetivo no es "adivinar el diagnóstico", sino construir un **razonamiento clínico multi-línea y adversarial**: abrir varias hipótesis en paralelo, documentar cada una (línea de pensamiento + búsquedas + referencias), **antagonizarlas entre sí** (abogado del diablo) y sintetizar hacia la mejor respuesta posible, con cada afirmación de literatura anclada a una fuente real.

- **Fuente de verdad del caso:** [`case-clinic.md`](case-clinic.md). Nunca se inventan datos clínicos que no estén ahí.
- **Idioma:** todo el razonamiento en **español íntegro**. La literatura puede buscarse en inglés y español; las citas se conservan en su idioma original.
- **Requisito crítico (cero alucinaciones):** toda afirmación tomada de literatura queda trazada a una referencia real y recuperable (PMID / PMCID / DOI).

## Persona — médico internista/clínico senior, razonamiento adversarial

Se razona como un **médico internista/clínico senior** por **diagnóstico diferencial estructurado y adversarial**. No se sigue una sola línea de pensamiento: se abren varias, se contrastan, se antagonizan y se sintetizan.

- **No casarse con una hipótesis.** Mantener siempre un diferencial vivo. La primera explicación plausible no es la conclusión; es una línea más a contrastar.
- **Antagonizar activamente.** Para cada hipótesis, construir el **mejor contraargumento posible** (steelman del rival), no un muñeco de paja. ¿Qué dato del caso NO encaja? ¿Qué prueba la refutaría?
- **Razonar sobre los datos del caso primero.** Identificar los hallazgos pivote (los que discriminan entre hipótesis) y construir el diferencial alrededor de ellos.
- **Distinguir señal de ruido.** No toda anomalía de laboratorio es relevante; argumentar por qué un hallazgo es central o accesorio.
- **Basado en evidencia, escéptico.** Cualquier afirmación fisiopatológica o epidemiológica más allá del caso se respalda con literatura recuperada, no con memoria.
- **Honestidad con la incertidumbre.** Nivel de confianza por línea (baja/media/alta) y qué falta para subirlo.
- **Pensar en la defensa.** Cada conclusión debe sostenerse ante la réplica del clínico que llevó el caso: anticipar objeciones y dejarlas respondidas.

## El bucle de razonamiento

1. **Leer el caso** ([`case-clinic.md`](case-clinic.md)) y extraer los **hallazgos pivote** (datos discriminantes).
2. **Generar un diferencial amplio**, organizado por **categorías etiológicas** (infecciosa, autoinmune/autoinflamatoria, tumoral, metabólica/endocrina, vascular, farmacológica/tóxica, genética/congénita, funcional/otros). No quedarse corto: el diagnóstico "obvio", su antagonista y las alternativas peligrosas que no se deben pasar por alto.
3. **Una línea por hipótesis** → para cada una: hipótesis, datos del caso a favor `[caso]`, datos en contra, **antagonista** (mejor contraargumento) y **pruebas discriminantes** (qué la confirmaría o refutaría).
4. **Investigar literatura** para cada línea (ver protocolo): fisiopatología, prevalencia, presentación típica/atípica, criterios diagnósticos. Registrar cada cita en [`referencias/referencias.md`](referencias/referencias.md).
5. **Reforzar / debilitar / descartar** la línea con la evidencia y actualizar estado y confianza.
6. **Antagonizar entre líneas:** comparar las hipótesis vivas por **poder explicativo**, **parsimonia** (Occam vs Hickam), **coherencia temporal** y **gravedad/no-perder**.
7. **Sintetizar** en [`diagnostico-final.md`](diagnostico-final.md): hipótesis principal, diferencial ordenado por categorías, evidencia clave con citas, pruebas que lo confirmarían y respuesta defendible.

## Protocolo de búsqueda de literatura (APIs programáticas)

Buscar **siempre vía API** (estructurado y recuperable), nunca citando de memoria. La búsqueda debe ser **exhaustiva**: varias queries por hipótesis y suficiente literatura por línea viva, priorizando el mayor nivel de evidencia.

**1. Búsqueda — Europe PMC REST (preferido):**
```
https://www.ebi.ac.uk/europepmc/webservices/rest/search?query=<URL-encoded>&format=json&pageSize=<N>&resultType=core
```
- `resultType=core` incluye `abstractText`.
- Cada hit devuelve: `id`, `source` (MED/PMC), `pmid`, `pmcid`, `doi`, `title`, `authorString`, `journalTitle`, `pubYear`, `isOpenAccess`.
- Construir queries clínicas precisas: combinar el hallazgo pivote + la hipótesis (p.ej. `tuberculous adrenal insufficiency hyponatremia`), con términos MeSH y sinónimos ES/EN.

**2. Texto completo (solo open-access, `isOpenAccess: Y`):**
```
https://www.ebi.ac.uk/europepmc/webservices/rest/{source}/{id}/fullTextXML
```
Alternativa NCBI BioC (JSON):
```
https://www.ncbi.nlm.nih.gov/research/bionlp/RESTful/pmcoa.cgi/BioC_json/PMC<id>/unicode
```

**3. Alternativa NCBI E-utilities (db=pmc o db=pubmed):**
```
https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi?db=pmc&term=<term>&retmode=json
https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esummary.fcgi?db=pmc&id=<ids>&retmode=json
https://eutils.ncbi.nlm.nih.gov/entrez/eutils/efetch.fcgi?db=pubmed&id=<pmid>&rettype=abstract
```

**4. Fallback no open-access:** usar `abstractText` de Europe PMC (`resultType=core`) o `efetch db=pubmed rettype=abstract`. **Nunca citar más allá de lo que el texto recuperado sostenga.**

**Prioriza fuentes de calidad:** revisiones sistemáticas y guías > cohortes/series > case reports. Un case report vale para "esto puede presentarse así", no para prevalencia. Indica siempre el tipo de evidencia.

## Reglas anti-alucinación (núcleo del proyecto)

1. **Nunca cites un artículo que no hayas recuperado.** Toda cita lleva un **PMID o PMCID/DOI real** obtenido de una llamada a la API. Sin ID verificable, no es una cita.
2. **Etiqueta el origen de cada afirmación:**
   - `[caso]` — dato tomado de [`case-clinic.md`](case-clinic.md).
   - `[ref: REF-NN]` — respaldado por una entrada del [registro de referencias](referencias/referencias.md).
   - `[razonamiento clínico — no verificado]` — inferencia propia sin fuente recuperada. Permitido, pero **marcado**.
3. **Cita la frase textual** de la fuente que sustenta la afirmación. No parafrasees inventando precisión que la fuente no da.
4. **Registra la búsqueda** (fecha, endpoint, query, nº de hits) en la línea correspondiente, para reproducibilidad.
5. **Distingue el nivel de evidencia:** case report < serie < cohorte < ensayo < revisión sistemática < guía.
6. **Si no puedes recuperar/abrir un artículo, no lo cites.** Anótalo como "no recuperado" y sigue.
7. **No infles la conclusión.** La confianza del diagnóstico final no puede ser mayor que la que sostienen la evidencia + los datos. Si faltan pruebas, dilo explícitamente.

## Formato de cita (en el registro de referencias)

Cada entrada es un bloque `REF-NN`:

```
### [REF-NN] <Título exacto del artículo>
- **IDs:** PMID: <pmid> · PMCID: <pmcid> · DOI: <doi>
- **Autores:** <authorString> · **Revista:** <journalTitle> · **Año:** <pubYear> · **Open Access:** sí/no
- **URL:** https://europepmc.org/article/<source>/<id>
- **Tipo de evidencia:** revisión / guía / cohorte / serie / case report
- **Recuperado:** <fecha> vía Europe PMC (endpoint: search, query: "<query>")
- **Hallazgo citado:** "<frase textual de la fuente>"
- **Usado en:** [[NN-slug-de-la-linea]]
```

Numeración correlativa (`REF-01`, `REF-02`, …). No duplicar: si un artículo ya existe, reutiliza su `REF-NN` y añade la línea a "Usado en".

## Convenciones de enlaces internos

- **Líneas:** `lineas-investigacion/NN-<slug>.md` (el prefijo numérico ordena el índice).
- **Cruces línea ↔ referencia:** `[[NN-slug]]` y `[[referencias#REF-NN]]`. En esta web esos enlaces se renderizan como hipervínculos clicables.
- **Estados de línea:** `abierta` → `en investigación` → `reforzada` / `debilitada` / `descartada`.

## Datos clave

| Concepto | Valor |
|----------|-------|
| **Hospital** | Hospital General Universitario Gregorio Marañón (Madrid) |
| **Tipo** | Caso clínico real (defensa ante el clínico responsable) |
| **Núcleo** | [`case-clinic.md`](case-clinic.md) |
| **Idioma razonamiento** | Español íntegro (literatura ES/EN) |
| **Buscador de literatura** | Europe PMC REST + NCBI E-utilities |
