# Registro maestro de referencias

> Registro único y citable de toda la literatura usada en el caso. **Regla de oro: ninguna afirmación de literatura sin una entrada `REF-NN` aquí, con PMID/PMCID/DOI real recuperado vía API.** Numeración correlativa. No duplicar: si un artículo ya existe, reutiliza su `REF-NN` y añade la línea a "Usado en".

## Cómo se llena (resumen del protocolo)

1. Buscar vía Europe PMC REST (`.../search?query=...&format=json&resultType=core`) o NCBI E-utilities.
2. Recuperar texto completo (OA) o abstract; extraer la **frase textual** que sustenta la afirmación.
3. Crear/actualizar la entrada `REF-NN` con el formato de abajo.
4. Enlazar desde la línea con `[[referencias#REF-NN]]`.

Detalles completos del protocolo y los endpoints en [Metodología y protocolo de búsqueda](../metodologia.md).

## Formato de entrada

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

---

## Referencias

### [REF-01] Think Addison's Disease: Disseminated Tuberculosis Presenting With Adrenal Crisis in a Young Male Patient.
- **IDs:** PMID: 41210058 · PMCID: PMC12592887 · DOI: 10.7759/cureus.94091
- **Autores:** Mohamed H, Attia AM, John HT, Owies A, Varrier M. · **Revista:** Cureus · **Año:** 2025 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41210058
- **Tipo de evidencia:** case report
- **Recuperado:** 2026-06-18 vía Europe PMC (endpoint: search, query: "hyponatremia hyperkalemia primary adrenal insufficiency Addison prevalence")
- **Hallazgo citado:** "profound hyponatremia (Na 106 mmol/L) with hyperkalaemia (K 5.6 mmol/L)" — varón joven con TB diseminada que debuta como crisis suprarrenal, con hiperpigmentación y aumento adrenal bilateral. Caso espejo del nuestro (varón joven, contexto TB, hiponatremia grave).
- **Usado en:** [[01-insuficiencia-suprarrenal-primaria]], [[05-tuberculosis-sistemica]]

### [REF-02] Pathophysiology, symptoms, outcomes, and evaluation of hyponatremia: comprehension and best clinical practice.
- **IDs:** PMID: 39847311 · PMCID: PMC11828805 · DOI: 10.1007/s10157-025-02624-9
- **Autores:** Sumi H, Tominaga N, Fujita Y, Verbalis JG, and the Electrolyte Winter Seminar Collaborative Group. · **Revista:** Clinical and Experimental Nephrology · **Año:** 2025 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/39847311
- **Tipo de evidencia:** revisión
- **Recuperado:** 2026-06-18 vía Europe PMC (endpoint: fullText BioC PMC11828805, query: "nausea vomiting stimulus vasopressin ADH secretion hyponatremia")
- **Hallazgo citado:** "Decreased effective arterial blood volume (EABV) and non-osmotic stimuli, including pain, nausea, and stress, cause AVP secretion independently of POsm." (también: "non-osmotic AVP secretory stimuli, including pain, nausea, and stress, easily lead to impaired free water excretion")
- **Usado en:** [[02-hiponatremia-hipovolemica-vomitos]], [[03-siadh]]

### [REF-03] Adrenal infections update: how radiologists can contribute to patient care.
- **IDs:** PMID: 39932870 · PMCID: PMC11919078 · DOI: 10.1093/bjr/tqaf025
- **Autores:** Abreu-Gomez J, Murad V, Ezzat S, Navin PJ, Westphalen AC. · **Revista:** The British Journal of Radiology · **Año:** 2025 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/39932870
- **Tipo de evidencia:** revisión
- **Recuperado:** 2026-06-18 vía Europe PMC (endpoint: fullText BioC PMC11919078, query: "adrenal tuberculosis CT imaging size calcification enlargement atrophy")
- **Hallazgo citado:** "In the setting of active tuberculosis, particularly in pulmonary cases, the adrenals often display thickening and increased size, usually in a bilateral fashion." · "Conversely, atrophic and calcified glands are indicative of remote or inactive infection." · "over 90% gland destruction required before hormone insufficiency becomes apparent and therefore, asymptomatic infection is not uncommon with clinical manifestations not apparent even after years."
- **Usado en:** [[05-tuberculosis-sistemica]], [[01-insuficiencia-suprarrenal-primaria]]

### [REF-04] Addisonian Pigmentation - The Great Mimicker - A Review.
- **IDs:** PMID: 39649977 · PMCID: PMC11623411 · DOI: 10.4103/ijd.ijd_234_23
- **Autores:** Verma D, Sarkar R, Mendiratta V, Srivastava A. · **Revista:** Indian Journal of Dermatology · **Año:** 2024 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/39649977
- **Tipo de evidencia:** revisión
- **Recuperado:** 2026-06-18 vía Europe PMC (endpoint: search, query: "tuberculosis cause Addison disease primary adrenal insufficiency developing countries")
- **Hallazgo citado:** "The most common cause of adrenal insufficiency in developing countries is tuberculosis."
- **Usado en:** [[05-tuberculosis-sistemica]]

### [REF-05] Primary adrenal insufficiency and systemic tuberculosis in a 10-year-old boy: case report.
- **IDs:** PMID: 40498941 · PMCID: PMC12176017 · DOI: 10.17843/rpmesp.2025.421.14092
- **Autores:** Schult-Montoya S, Lindo-Pérez FR. · **Revista:** Revista Peruana de Medicina Experimental y Salud Pública · **Año:** 2025 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/40498941
- **Tipo de evidencia:** case report
- **Recuperado:** 2026-06-18 vía Europe PMC (endpoint: search, query: "tuberculosis cause Addison disease primary adrenal insufficiency developing countries")
- **Hallazgo citado:** "Tuberculosis is one of the main causes [of primary adrenal insufficiency] in developing countries." (paciente latinoamericano con insuficiencia suprarrenal primaria por TB sistémica)
- **Usado en:** [[05-tuberculosis-sistemica]]

### [REF-06] Unmasking a rare and dangerous trio in early pregnancy: hyperemesis gravidarum complicated by transient thyrotoxicosis and starvation ketoacidosis.
- **IDs:** PMID: 41491687 · PMCID: PMC12870128 · DOI: 10.1186/s12902-025-02150-5
- **Autores:** Hroub MR, Mohsen M, Hijazy A, Jamal LMA, Atrash B, Ramzi M, Atrash J. · **Revista:** BMC Endocrine Disorders · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41491687
- **Tipo de evidencia:** case report
- **Recuperado:** 2026-06-18 vía Europe PMC (endpoint: search, query: "vomiting metabolic alkalosis hypokalemia hypochloremia pathophysiology review")
- **Hallazgo citado:** "While the typical biochemical profile [of intractable vomiting/hyperemesis] includes hypochloremic, hypokalemic metabolic alkalosis..." — establece que el vómito prolongado "puro" tiende a producir hipopotasemia y alcalosis, patrón **ausente** en nuestro paciente (K alto-normal, sin alcalosis).
- **Usado en:** [[02-hiponatremia-hipovolemica-vomitos]]

### [REF-07] [Adrenal Insufficiency: Etiology and Characterization of Patients Attended at a University Center].
- **IDs:** PMID: 40358484 · PMCID: — · DOI: 10.4067/s0034-98872025000300162
- **Autores:** Araya AV, Pineda P, Cordero F, Ávila D, González J. · **Revista:** Revista Médica de Chile · **Año:** 2025 · **Open Access:** no (abstract recuperado vía API)
- **URL:** https://europepmc.org/article/MED/40358484
- **Tipo de evidencia:** cohorte retrospectiva (102 pacientes; 40 con insuficiencia suprarrenal primaria)
- **Recuperado:** 2026-06-18 vía Europe PMC (endpoint: search resultType=core, query: "ext_id:40358484 src:med")
- **Hallazgo citado:** "The most frequent etiologies were: Addison's disease (AD) (65%) in PAI..." · "Symptoms such as asthenia, weight loss, abdominal pain and muscle fatigue were significantly more frequent in PAI." · "We observed a trend to hyponatremia, hypercalcemia and in PAI, although to hyperkalemia and increased ACTH and plasma renin activity." · "Fifty eight percent of patients with AD (15/26) had associated autoimmune thyroid disorders."
- **Usado en:** [[01-insuficiencia-suprarrenal-primaria]]

### [REF-08] The "Polyglandular Crisis" Behind Recurrent Hyponatremia: Misdiagnosis of a Case of Autoimmune Polyglandular Syndrome Type 2.
- **IDs:** PMID: 41659856 · PMCID: PMC12872557 · DOI: 10.3389/fimmu.2026.1744295
- **Autores:** Yan M, Wu H, Deng J, Wang Y, Huang H, Wei H. · **Revista:** Frontiers in Immunology · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41659856
- **Tipo de evidencia:** case report + revisión de literatura
- **Recuperado:** 2026-06-18 vía Europe PMC (endpoint: search, query: "primary adrenal insufficiency presenting symptoms hyponatremia frequency diagnostic delay")
- **Hallazgo citado:** "...characterized predominantly by emaciation, fatigue, palpitations, and notably, refractory hyponatremia." · "The case was marked by highly non-specific clinical manifestations, which resulted in multiple episodes of misdiagnosis and missed diagnosis throughout her course of treatment." — insuficiencia suprarrenal (autoinmune) que debuta como hiponatremia refractoria/recidivante repetidamente mal diagnosticada.
- **Usado en:** [[01-insuficiencia-suprarrenal-primaria]]

---

> **2ª ronda (2026-06-21) — diferencial exhaustivo por categorías etiológicas (REF-09 a REF-71).** Recuperadas vía Europe PMC REST (`resultType=core`) y NCBI E-utilities en esta sesión; verificación cruzada de muestra (REF-10, REF-21, REF-52, REF-56) por consulta directa `EXT_ID`.

### 🧬 GENÉTICA / CONGÉNITA

### [REF-09] X-linked adrenoleukodystrophy and primary adrenal insufficiency.
- **IDs:** PMID: 38034003 · PMCID: PMC10687143 · DOI: 10.3389/fendo.2023.1309053
- **Autores:** Cappa M, Todisco T, Bizzarri C. · **Revista:** Frontiers in Endocrinology · **Año:** 2023 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/38034003
- **Tipo de evidencia:** revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "X-linked adrenoleukodystrophy adrenal insufficiency young men")
- **Hallazgo citado:** "Primary adrenal insufficiency (PAI) is one of the main features of X-ALD, with a prevalence of 70% in ALD/AMN patients... A growing consensus supports VLCFA assessment in all male children presenting with PAI."
- **Usado en:** [[14-adrenoleucodistrofia-x]]

### [REF-10] Primary adrenal insufficiency resulting in diagnosis of rare ABCD1 pathogenic variant in X-linked adrenoleukodystrophy.
- **IDs:** PMID: 42112257 · PMCID: PMC13155115 · DOI: 10.1210/jcemcr/luag124
- **Autores:** Jin A, Bhatnagar A, Bryant A, Soe K. · **Revista:** JCEM Case Reports · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/42112257
- **Tipo de evidencia:** case report
- **Recuperado:** 2026-06-21 vía Europe PMC (search EXT_ID:42112257 — verificado en esta sesión)
- **Hallazgo citado:** "We report a case of a 32-year-old African American male with adult-onset X-ALD presenting with primary adrenal insufficiency (PAI)... negative 21-alpha-hydroxylase antibodies and elevated plasma very long chain fatty acids... the importance of screening plasma very long chain fatty acid levels after ruling out common etiologies."
- **Usado en:** [[14-adrenoleucodistrofia-x]]

### [REF-11] Clinical and radiological characteristics of adult-onset X-linked adrenoleukodystrophy: a Chinese cohort study and review of the literature.
- **IDs:** PMID: 41094371 · PMCID: PMC12523032 · DOI: 10.1186/s12883-025-04449-1
- **Autores:** Xiao H, Huang H, Chen Y, et al. · **Revista:** BMC Neurology · **Año:** 2025 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41094371
- **Tipo de evidencia:** serie de casos + revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "adrenoleukodystrophy isolated adrenal insufficiency males VLCFA screening")
- **Hallazgo citado:** "Routine screening for ALD should be conducted in male patients diagnosed with Addison's disease... Elevated levels of VLCFA function as a reliable clinical biomarker for ALD."
- **Usado en:** [[14-adrenoleucodistrofia-x]]

### [REF-12] Adrenal insufficiency and the use of mineralocorticoid treatment in male patients with adrenoleukodystrophy.
- **IDs:** PMID: 39252037 · PMCID: PMC11382501 · DOI: 10.1186/s12902-024-01712-3
- **Autores:** Zekarias KL, Salim M, Tessier KM, Radulescu A. · **Revista:** BMC Endocrine Disorders · **Año:** 2024 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/39252037
- **Tipo de evidencia:** cohorte retrospectiva (n=437)
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "X-linked adrenoleukodystrophy adrenal insufficiency young men")
- **Hallazgo citado:** "Of the male ALD patients, 60% (213 out of 358) had a diagnosis of AI, and 39% (84 out of 213) of those with AI were prescribed mineralocorticoid replacement therapy."
- **Usado en:** [[14-adrenoleucodistrofia-x]]

### [REF-13] Adrenoleukodystrophy in adults: phenotypic characterisation and natural history in a large cohort.
- **IDs:** PMID: 41667276 · PMCID: PMC13217074 · DOI: 10.1136/jnnp-2025-337540
- **Autores:** Benzoni C, Moscatelli M, Lanteri P, et al. · **Revista:** J Neurol Neurosurg Psychiatry · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41667276
- **Tipo de evidencia:** cohorte observacional (n=140)
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "adrenomyeloneuropathy Addison primary adrenal insufficiency")
- **Hallazgo citado:** "Adrenomyeloneuropathy (AMN) predominated in males... Males had higher very long-chain fatty acid (VLCFA) levels than females."
- **Usado en:** [[14-adrenoleucodistrofia-x]]

### [REF-14] Case Report: ...non-classical congenital adrenal hyperplasia in a Chinese girl (CYP21A2).
- **IDs:** PMID: 41988147 · PMCID: PMC13076340 · DOI: 10.3389/fped.2026.1778805
- **Autores:** Li N, Lu C, Gu HF, An X. · **Revista:** Frontiers in Pediatrics · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41988147
- **Tipo de evidencia:** case report
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "non-classic congenital adrenal hyperplasia adult")
- **Hallazgo citado:** "The non-classic form of CAH (NCCAH) often occurs in late puberty or in young adults due to a mild excess in postnatal androgen synthesis... hyperandrogenism... adrenal hyperplasia."
- **Usado en:** [[15-hiperplasia-suprarrenal-congenita]]

### [REF-15] Unveiling Salt-Wasting Congenital Adrenal Hyperplasia in an Infant: A Diagnostic Challenge.
- **IDs:** PMID: 41809282 · PMCID: PMC12968897 · DOI: 10.7759/cureus.103140
- **Autores:** Kummari S, Krishna Sravya M, R M. · **Revista:** Cureus · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41809282
- **Tipo de evidencia:** case report
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "congenital adrenal hyperplasia salt wasting hyponatremia")
- **Hallazgo citado:** "the salt-wasting type is the most severe form of CAH... 17-OH-progesterone levels at 109.19 ng/mL... hyponatremia (111 mmol/L), hyperkalemia (6.0 mmol/L)." (presentación INFANTIL)
- **Usado en:** [[15-hiperplasia-suprarrenal-congenita]]

### 🛡️ AUTOINMUNE / AUTOINFLAMATORIA · 📋 GUÍA DE REFERENCIA

### [REF-16] Diagnosis and Treatment of Primary Adrenal Insufficiency: An Endocrine Society Clinical Practice Guideline.
- **IDs:** PMID: 26760044 · PMCID: PMC4880116 · DOI: 10.1210/jc.2015-1710
- **Autores:** Bornstein SR, Allolio B, Arlt W, et al. · **Revista:** J Clin Endocrinol Metab · **Año:** 2016 · **Open Access:** no (abstract vía core)
- **URL:** https://europepmc.org/article/MED/26760044
- **Tipo de evidencia:** GUÍA de práctica clínica (Endocrine Society)
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "primary adrenal insufficiency Addison diagnosis management guideline 21-hydroxylase")
- **Hallazgo citado:** "We recommend a short corticotropin test (250 μg) as the 'gold standard' diagnostic tool to establish the diagnosis." · "Diagnosis of the underlying cause should include a validated assay of autoantibodies against 21-hydroxylase. In autoantibody-negative individuals, other causes should be sought."
- **Usado en:** [[01-insuficiencia-suprarrenal-primaria]], [[08-adrenalitis-autoinmune-aps]], [[14-adrenoleucodistrofia-x]]

### [REF-17] Female fertility and pregnancy in autoimmune Addison's disease - a mini review.
- **IDs:** PMID: 40607215 · PMCID: PMC12216664 · DOI: 10.3389/fendo.2025.1510815
- **Autores:** O'Murchadha L, Pazderska A. · **Revista:** Frontiers in Endocrinology · **Año:** 2025 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/40607215
- **Tipo de evidencia:** revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search EXT_ID:40607215)
- **Hallazgo citado:** "Autoimmune Addison's Disease (AAD) is by far the most common cause of primary adrenal insufficiency in developed countries, occurring more commonly in women compared with men."
- **Usado en:** [[08-adrenalitis-autoinmune-aps]]

### [REF-18] An overview of inborn errors of metabolism manifesting with primary adrenal insufficiency.
- **IDs:** PMID: 29956047 · PMCID: PMC6204320 · DOI: 10.1007/s11154-018-9447-2
- **Autores:** Hannah-Shmouni F, Stratakis CA. · **Revista:** Rev Endocr Metab Disord · **Año:** 2018 · **Open Access:** no (abstract vía core)
- **URL:** https://europepmc.org/article/MED/29956047
- **Tipo de evidencia:** revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "primary adrenal insufficiency Addison diagnosis management guideline 21-hydroxylase")
- **Hallazgo citado:** "The most common causes of PAI are autoimmune adrenalitis (Addison's disease), infectious diseases, adrenalectomy, neoplasia, medications, and various rare genetic syndromes... prevalence of PAI in Western countries is approximately 140 cases per million."
- **Usado en:** [[08-adrenalitis-autoinmune-aps]]

### [REF-19] Latent Adrenal Insufficiency: From Concept to Diagnosis.
- **IDs:** PMID: 34512551 · PMCID: PMC8429826 · DOI: 10.3389/fendo.2021.720769
- **Autores:** Younes N, Bourdeau I, Lacroix A. · **Revista:** Frontiers in Endocrinology · **Año:** 2021 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/34512551
- **Tipo de evidencia:** revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "Addison disease presenting features hyponatremia hyperkalemia prevalence at diagnosis cohort")
- **Hallazgo citado:** "Patients present with hallmark manifestations including fatigue, weight loss, abdominal pain, melanoderma, hypotension, salt craving, hyponatremia, hyperkalemia, or acute adrenal crisis. Diagnosis is established by unequivocally low morning serum cortisol/aldosterone and elevated ACTH and renin concentrations."
- **Usado en:** [[01-insuficiencia-suprarrenal-primaria]], [[08-adrenalitis-autoinmune-aps]]

### [REF-20] Prevalence of Various Systemic and Organ-Specific Autoimmune Markers in Addison's Disease Patients Compared to Healthy Controls.
- **IDs:** PMID: 40507712 · PMCID: PMC12155909 · DOI: 10.3390/jcm14113951
- **Autores:** Feyzullova A, Kirilov G, Elenkova A, et al. · **Revista:** J Clin Med · **Año:** 2025 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/40507712
- **Tipo de evidencia:** cohorte caso-control
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "autoimmune Addison disease 21-hydroxylase antibodies")
- **Hallazgo citado:** "21-hydroxylase autoantibodies (21OHAb), glutamic acid decarboxylase autoantibodies (GADAbs)... were measured in all participants."
- **Usado en:** [[08-adrenalitis-autoinmune-aps]]

### [REF-21] An Intriguing Case Report of Type 2 Autoimmune Polyendocrine Syndrome Post-SARS-CoV-2.
- **IDs:** PMID: 40849756 · PMCID: — · DOI: 10.2174/0118715303407830250807114958
- **Autores:** Voltan G, Graziani A, Torchio M, Mian C, Betterle C, Sabbadin C. · **Revista:** Endocr Metab Immune Disord Drug Targets · **Año:** 2025 · **Open Access:** no (abstract vía core)
- **URL:** https://europepmc.org/article/MED/40849756
- **Tipo de evidencia:** case report + mini-revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "autoimmune polyendocrine syndrome type 2 adrenal insufficiency Addison")
- **Hallazgo citado:** "We report the case of a 36-year-old male who developed APS-2... asthenia, hypotension, gastrointestinal symptoms, and weight loss. Laboratory investigations revealed undetectable morning cortisol, positive 21-hydroxylase and thyroid-peroxidase autoantibodies, elevated ACTH and renin."
- **Usado en:** [[08-adrenalitis-autoinmune-aps]]

### [REF-22] Delayed diagnosis of the full triad autoimmune polyendocrine syndrome type 2 with adrenal crisis: a case report and literature review.
- **IDs:** PMID: 40416965 · PMCID: PMC12098416 · DOI: 10.3389/fimmu.2025.1563629
- **Autores:** Yao Z, Chen H, Hu X, Ge D, Xu X, Xu D. · **Revista:** Frontiers in Immunology · **Año:** 2025 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/40416965
- **Tipo de evidencia:** case report + revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "autoimmune polyendocrine syndrome type 2 adrenal insufficiency Addison")
- **Hallazgo citado:** "On admission, she was in hypovolemic shock and severe hyponatremia (118.0 mmol/L). Laboratory tests revealed low basal cortisol (2.38 μg/dL) and markedly elevated adrenocorticotropic hormone (>1250 pg/mL)... persistent hyponatremia... resolved following fludrocortisone acetate supplementation."
- **Usado en:** [[08-adrenalitis-autoinmune-aps]]

### 🦠 INFECCIOSA

### [REF-23] Etiology, clinical characteristics and mortality among Indian patients with Addison's disease.
- **IDs:** PMID: 36625588 · PMCID: PMC9986409 · DOI: 10.1530/EC-22-0439
- **Autores:** Gunna S, Singh M, Pandey R, Marak RSK, Aggarwal A, Mohanta B, Yu L, Bhatia E. · **Revista:** Endocrine Connections · **Año:** 2023 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/36625588
- **Tipo de evidencia:** cohorte etiológica (n=89 PAI; biopsia adrenal en 60)
- **Recuperado:** 2026-06-21 vía Europe PMC (search EXT_ID:36625588 — verificado en esta sesión)
- **Hallazgo citado:** "The most frequent etiologies of PAI were adrenal histoplasmosis (AH, 45%), adrenal tuberculosis (AT, 15%), autoimmunity (AI, 25%) and primary lymphoma (6%)... AH and AT could not be differentiated on the basis of clinical features... Mortality was significantly higher in AH (45%) compared with AT (8%) or AI (5%)."
- **Usado en:** [[06-paracoccidioidomicosis]], [[07-histoplasmosis-micosis]], [[05-tuberculosis-sistemica]]

### [REF-24] Adrenal Histoplasmosis and Tuberculosis: Clinical Presentations and a High Prevalence of Adrenal Insufficiency.
- **IDs:** PMID: 40205654 · PMCID: — · DOI: 10.1111/cen.15246
- **Autores:** Vorasayun T, Pengkhum P, Thavaraputta S, et al. · **Revista:** Clin Endocrinol (Oxf) · **Año:** 2025 · **Open Access:** no (abstract vía efetch)
- **URL:** https://europepmc.org/article/MED/40205654
- **Tipo de evidencia:** estudio retrospectivo comparativo (n=35)
- **Recuperado:** 2026-06-21 vía NCBI efetch (query: "histoplasmosis adrenal insufficiency")
- **Hallazgo citado:** "Bilateral adrenal abnormalities were seen in 91%, and all patients with unilateral lesions later developed contralateral involvement. Adrenal lesions ranged from enlargement to mass sized 9.8 cm. The prevalence of AI was 74%."
- **Usado en:** [[07-histoplasmosis-micosis]], [[05-tuberculosis-sistemica]]

### [REF-25] Acquired perforating dermatosis and Addison's disease due to disseminated histoplasmosis.
- **IDs:** PMID: 24194970 · PMCID: PMC3772918 · DOI: 10.4161/derm.22677
- **Autores:** Choudhary N, Aggarwal I, Dutta D, et al. · **Revista:** Dermatoendocrinol · **Año:** 2013 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/24194970
- **Tipo de evidencia:** case report
- **Recuperado:** 2026-06-21 vía NCBI efetch (query: "histoplasmosis adrenal insufficiency")
- **Hallazgo citado:** "presented with features of adrenal insufficiency (nausea vomiting, hypotension and increased pigmentation)... enlarged bilateral adrenals with hepatosplenomegaly on CT."
- **Usado en:** [[07-histoplasmosis-micosis]]

### [REF-26] Adrenocortical dysfunction in paracoccidioidomycosis...
- **IDs:** PMID: 1330381 · PMCID: — · DOI: 10.1111/j.1365-2265.1992.tb02263.x
- **Autores:** Moreira AC, Martinez R, Castro M, Elias LL. · **Revista:** Clin Endocrinol (Oxf) · **Año:** 1992 · **Open Access:** no (abstract vía efetch)
- **URL:** https://europepmc.org/article/MED/1330381
- **Tipo de evidencia:** cohorte prospectiva (47 varones)
- **Recuperado:** 2026-06-21 vía NCBI efetch (query: "paracoccidioidomycosis adrenal insufficiency")
- **Hallazgo citado:** "Paracoccidioidomycosis is an important cause of Addison's disease in South America... The frequency of Addison's disease among our patients with paracoccidioidomycosis was 10%."
- **Usado en:** [[06-paracoccidioidomicosis]]

### [REF-27] Paracoccidioidomycosis and Addison's syndrome - case report.
- **IDs:** PMID: 36718536 · PMCID: — · DOI: 10.1177/00494755231153197
- **Autores:** Lazzaretti GS, Sena LMC, Corrêa A, et al. · **Revista:** Tropical Doctor · **Año:** 2023 · **Open Access:** no (abstract vía efetch)
- **URL:** https://europepmc.org/article/MED/36718536
- **Tipo de evidencia:** case report
- **Recuperado:** 2026-06-21 vía NCBI efetch (query: "paracoccidioidomycosis adrenal gland involvement Addison")
- **Hallazgo citado:** "more prevalent in men, between 30 and 60 years old, commonly rural workers... adrenal involvement being observed in 5% of cases and requiring the destruction of 80% of the glands for symptoms of adrenal insufficiency to appear."
- **Usado en:** [[06-paracoccidioidomicosis]]

### [REF-28] [Adrenal gland insufficiency secondary to paracoccidioidomycosis].
- **IDs:** PMID: 12404928 · PMCID: — · DOI: —
- **Autores:** Oñate JM, Tobón AM, Restrepo A. · **Revista:** Biomédica · **Año:** 2002 · **Open Access:** —
- **URL:** https://europepmc.org/article/MED/12404928
- **Tipo de evidencia:** serie / revisión de registros
- **Recuperado:** 2026-06-21 vía NCBI efetch (query: "paracoccidioidomicosis suprarrenal")
- **Hallazgo citado:** "Paracoccidioidomycosis is regularly associated with adrenal insufficiency in 10-15% of symptomatic cases... All patients experienced weight loss and malaise; all had abnormal lung X-rays."
- **Usado en:** [[06-paracoccidioidomicosis]]

### [REF-29] Addison's disease due to adrenal tuberculosis: contrast-enhanced CT features and clinical duration correlation.
- **IDs:** PMID: 17182208 · PMCID: — · DOI: 10.1016/j.ejrad.2006.11.025
- **Autores:** Guo YK, Yang ZG, Li Y, et al. · **Revista:** Eur J Radiol · **Año:** 2007 · **Open Access:** no (abstract vía efetch)
- **URL:** https://europepmc.org/article/MED/17182208
- **Tipo de evidencia:** serie radiológica (n=42 TB adrenal no tratada)
- **Recuperado:** 2026-06-21 vía NCBI efetch (query: "adrenal tuberculosis CT calcification atrophy")
- **Hallazgo citado:** "bilaterally enlarged adrenal glands were revealed in 38 cases (91%)... calcification in 21 cases (50%). As the duration of Addison's disease increased, the presence of calcification and contour preservation increased... whereas peripheral rim enhancement and mass-like enlargement decreased."
- **Usado en:** [[05-tuberculosis-sistemica]]

### [REF-30] Tuberculous Addison's disease: morphological and quantitative evaluation with multidetector-row CT.
- **IDs:** PMID: 17466476 · PMCID: — · DOI: 10.1016/j.ejrad.2006.12.012
- **Autores:** Ma ES, Yang ZG, Li Y, et al. · **Revista:** Eur J Radiol · **Año:** 2007 · **Open Access:** no (abstract vía efetch)
- **URL:** https://europepmc.org/article/MED/17466476
- **Tipo de evidencia:** serie radiológica (n=19)
- **Recuperado:** 2026-06-21 vía NCBI efetch (query: "adrenal tuberculosis CT calcification atrophy")
- **Hallazgo citado:** "Enlargement of the glands appeared in 18 cases (94.7%)... the remaining one case (5.3%) showed atrophy bilaterally... Calcification was revealed in 16 adrenals (42.1%), increasing in incidence with disease progression."
- **Usado en:** [[05-tuberculosis-sistemica]]

### [REF-31] Clinical significance of adrenal computed tomography in Addison's disease.
- **IDs:** PMID: 1294374 · PMCID: — · DOI: 10.1507/endocrj1954.39.563
- **Autores:** Sun ZH, Nomura K, Toraya S, et al. · **Revista:** Endocrinol Jpn · **Año:** 1992 · **Open Access:** no (abstract vía efetch)
- **URL:** https://europepmc.org/article/MED/1294374
- **Tipo de evidencia:** serie con seguimiento longitudinal (n=12)
- **Recuperado:** 2026-06-21 vía NCBI efetch (query: "adrenal tuberculosis CT calcification atrophy")
- **Hallazgo citado:** "In tuberculous Addison's disease... three of four patients examined during the first two years... had bilaterally enlarged adrenals... Thereafter, the adrenal glands may atrophy bilaterally, in contrast to adrenal glands in idiopathic Addison's disease, which atrophy bilaterally from disease onset... adrenal calcification was observed in five of eight patients with tuberculous Addison's disease, but not in idiopathic patients."
- **Usado en:** [[05-tuberculosis-sistemica]], [[08-adrenalitis-autoinmune-aps]]

### [REF-32] Current Approach for Diagnosis and Treatment of Adrenal Tuberculosis—Our Experience and Review of Literature.
- **IDs:** PMID: 35252566 · PMCID: PMC8894089 · DOI: 10.1055/s-0042-1743523
- **Autores:** Gupta S, Ansari MAM, Gupta AK, et al. · **Revista:** Surgery Journal (NY) · **Año:** 2022 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/35252566
- **Tipo de evidencia:** revisión + serie
- **Recuperado:** 2026-06-21 vía Europe PMC (search EXT_ID:35252566)
- **Hallazgo citado:** "in developing countries, it is still the most common cause of adrenal insufficiency... features of adrenal TB are bilateral adrenal enlargement and peripheral rim enhancement with or without calcifications."
- **Usado en:** [[05-tuberculosis-sistemica]]

### [REF-33] Bilateral adrenal cryptococcosis causing adrenal insufficiency in an immunocompetent patient.
- **IDs:** PMID: 38391340 · PMCID: — · DOI: 10.4103/ijpm.ijpm_185_22
- **Autores:** Kaur R, Mittal N, Soni A, Kaur H. · **Revista:** Indian J Pathol Microbiol · **Año:** 2024 · **Open Access:** no (abstract vía efetch)
- **URL:** https://europepmc.org/article/MED/38391340
- **Tipo de evidencia:** case report
- **Recuperado:** 2026-06-21 vía NCBI efetch (query: "cryptococcosis adrenal insufficiency")
- **Hallazgo citado:** "primary adrenal insufficiency and bilateral adrenal lesions, splenomegaly, and miliary mottling in the lungs... led toward the differential diagnosis of disseminated tuberculosis or fungal infection... keep the possibility of cryptococcosis in mind."
- **Usado en:** [[07-histoplasmosis-micosis]]

### 🎗️ TUMORAL / NEOPLÁSICA

### [REF-34] Primary adrenal insufficiency in patients with bilateral adrenal metastases treated with curative ablative radiation therapy: review and expert agreements.
- **IDs:** PMID: 42255979 · PMCID: PMC13234592 · DOI: 10.1016/j.ctro.2026.101195
- **Autores:** Bennassi A, Debbi K, Giraud N, et al. · **Revista:** Clin Transl Radiat Oncol · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/42255979
- **Tipo de evidencia:** revisión sistemática (PRISMA) + consenso
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "bilateral adrenal metastases primary adrenal insufficiency")
- **Hallazgo citado:** "PAI was reported in 47 patients (30%)... Time to onset ranged from 3 to 30 months."
- **Usado en:** [[09-neoplasia-suprarrenal-paraneoplasico]]

### [REF-35] Bilateral Adrenal Metastases From Breast Cancer 14 Years After Remission: Diagnostic Value of "Adrenal Thickening".
- **IDs:** PMID: 41694448 · PMCID: PMC12895272 · DOI: 10.1210/jcemcr/luaf258
- **Autores:** Martinez-Cruz M, Sharma S, Kannuswamy R, et al. · **Revista:** JCEM Case Reports · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41694448
- **Tipo de evidencia:** case report
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "bilateral adrenal metastases primary adrenal insufficiency")
- **Hallazgo citado:** "bilateral nodular adrenal enlargement with predominant nodules with attenuation >10 Hounsfield units (HU) and high fluorodeoxyglucose (FDG) avidity on PET-CT." (→ patrón OPUESTO a glándulas atróficas/hipodensas del caso)
- **Usado en:** [[09-neoplasia-suprarrenal-paraneoplasico]]

### [REF-36] The Immune Biology of the Adrenal Gland Microenvironment and Its Role in Metastatic Progression.
- **IDs:** PMID: 41683577 · PMCID: PMC12897121 · DOI: 10.3390/ijms27031153
- **Autores:** Liu NM, Sholevar CJ, Karimzadeh M, et al. · **Revista:** Int J Mol Sci · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41683577
- **Tipo de evidencia:** revisión narrativa
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "adrenal metastases series incidence adrenal insufficiency lung cancer")
- **Hallazgo citado:** "Metastatic lesions are the most common malignant tumor of the adrenal gland... most adrenal metastases occur in the context of disseminated disease."
- **Usado en:** [[09-neoplasia-suprarrenal-paraneoplasico]]

### [REF-37] Persistent adrenocortical insufficiency before and after treatment of lymphoma with marked adrenal enlargement - a case series.
- **IDs:** PMID: 40969788 · PMCID: PMC12440856 · DOI: 10.3389/fmed.2025.1632514
- **Autores:** Takiyama Y, Nanbu T, Sato T, et al. · **Revista:** Frontiers in Medicine · **Año:** 2025 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/40969788
- **Tipo de evidencia:** serie de casos (n=3)
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "primary adrenal lymphoma imaging bilateral adrenal enlargement CT")
- **Hallazgo citado:** "three cases with lymphoma with bilateral adrenal enlargement who presented with adrenal insufficiency... All three were diagnosed with adrenal insufficiency at presentation." (→ exige AUMENTO glandular, no atrofia)
- **Usado en:** [[09-neoplasia-suprarrenal-paraneoplasico]]

### [REF-38] Bilateral adrenal masses and adrenal insufficiency: a rare case of primary adrenal lymphoma.
- **IDs:** PMID: 41734456 · PMCID: PMC12936811 · DOI: 10.1530/edm-25-0148
- **Autores:** Eladl A, Michaelidou M, Gibb A, et al. · **Revista:** Endocrinol Diabetes Metab Case Rep · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41734456
- **Tipo de evidencia:** case report + revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "primary adrenal lymphoma bilateral adrenal insufficiency")
- **Hallazgo citado:** "Primary adrenal lymphoma (PAL) is a rare malignancy typically considered in patients presenting with features of adrenal insufficiency and bilateral adrenal gland enlargement... large bilateral adrenal masses with widespread lymph node involvement."
- **Usado en:** [[09-neoplasia-suprarrenal-paraneoplasico]]

### [REF-39] Primary Adrenal Gland Lymphoma: Report of 13 Cases—Polish Lymphoma Research Group Analysis.
- **IDs:** PMID: 41752871 · PMCID: PMC12941533 · DOI: 10.3390/life16020230
- **Autores:** Witkowska M, Kościelny K, Giza A, et al. · **Revista:** Life (Basel) · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41752871
- **Tipo de evidencia:** serie multicéntrica retrospectiva (n=13)
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "primary adrenal lymphoma bilateral adrenal insufficiency")
- **Hallazgo citado:** "The median age at the diagnosis was 69.1 years (range: 31-85)... 3 patients (23.5%) had bilateral lymphoma. Systemic symptoms (B symptoms) were observed in 11 out of 13 patients (85%)."
- **Usado en:** [[09-neoplasia-suprarrenal-paraneoplasico]]

### [REF-40] Tolvaptan for paraneoplastic SIADH in small cell lung cancer: a scoping review.
- **IDs:** PMID: 42119219 · PMCID: — · DOI: 10.1016/j.ctarc.2026.101233
- **Autores:** Cammann VL, Sheryl M, Fürst T, Jehle AW. · **Revista:** Cancer Treat Res Commun · **Año:** 2026 · **Open Access:** no (abstract vía efetch)
- **URL:** https://europepmc.org/article/MED/42119219
- **Tipo de evidencia:** scoping review (29 estudios, 86 pacientes)
- **Recuperado:** 2026-06-21 vía NCBI efetch (query: "paraneoplastic SIADH small cell lung cancer hyponatremia")
- **Hallazgo citado:** "Hyponatremia due to... SIADH occurs in approximately 25% of patients with small cell lung cancer (SCLC)... The median sodium concentration before initiation of tolvaptan was 117 mmol/L."
- **Usado en:** [[09-neoplasia-suprarrenal-paraneoplasico]]

### [REF-41] Endocrine paraneoplastic syndromes in lung cancer: A call for clinical vigilance (Review).
- **IDs:** PMID: 40083863 · PMCID: PMC11905218 · DOI: 10.3892/mco.2025.2831
- **Autores:** Koloutsou ME, Soura M, Andreikos D, et al. · **Revista:** Mol Clin Oncol · **Año:** 2025 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/40083863
- **Tipo de evidencia:** revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search EXT_ID:40083863)
- **Hallazgo citado:** "Common endocrine PNS in lung cancer include syndrome of inappropriate antidiuretic hormone secretion, hypercalcemia, Cushing syndrome..."
- **Usado en:** [[09-neoplasia-suprarrenal-paraneoplasico]]

### [REF-42] Refractory hyponatremia in small cell lung cancer: a case report and literature review.
- **IDs:** PMID: 41890180 · PMCID: PMC13013071 · DOI: 10.3389/fendo.2026.1780594
- **Autores:** Bao S, Qin L, Zhang Y, Jiang X, Duan L. · **Revista:** Frontiers in Endocrinology · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41890180
- **Tipo de evidencia:** case report + revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "ectopic ADH secretion malignancy hyponatremia euvolemic")
- **Hallazgo citado:** "Combined with features including high urinary sodium, euvolemic status, and normal renal function, the findings were consistent with a diagnosis of SIADH." (→ criterios que el caso NO cumple: TA 95/65, urea 59)
- **Usado en:** [[09-neoplasia-suprarrenal-paraneoplasico]], [[03-siadh]]

### ⚗️ METABÓLICA / ENDOCRINA

### [REF-43] Is there a causal relationship between hypothyroidism and hyponatremia?
- **IDs:** PMID: 37435527 · PMCID: PMC10331073 · DOI: 10.1177/20420188231180983
- **Autores:** Chen J. · **Revista:** Ther Adv Endocrinol Metab · **Año:** 2023 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/37435527
- **Tipo de evidencia:** revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "hyponatremia overt hypothyroidism severity relationship cross-sectional")
- **Hallazgo citado:** "if severe hyponatremia occurs in a patient without myxedema coma, other potential etiologies should be sought."
- **Usado en:** [[11-hipotiroidismo]]

### [REF-44] Myxedema coma: challenges and future directions, a systematic survey and review.
- **IDs:** PMID: 41053871 · PMCID: PMC12502585 · DOI: 10.1186/s13044-025-00268-1
- **Autores:** Zhang Y, Chu L, Han H. · **Revista:** Thyroid Research · **Año:** 2025 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41053871
- **Tipo de evidencia:** revisión sistemática
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "hypothyroidism hyponatremia mechanism pathophysiology")
- **Hallazgo citado:** "It is generally recommended to confirm the presence of decreased FT3 and/or FT4 levels as a necessary criterion for establishing a diagnosis of MC." (la hiponatremia grave tiroidea se asocia al coma mixedematoso, cuadro no presente en el caso)
- **Usado en:** [[11-hipotiroidismo]]

### [REF-45] Immune-Mediated Hypophysitis: An Updated Review.
- **IDs:** PMID: 42123046 · PMCID: PMC13163492 · DOI: 10.3390/jcm15093313
- **Autores:** Iglesias P. · **Revista:** J Clin Med · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/42123046
- **Tipo de evidencia:** revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "hypothyroidism hyponatremia mechanism pathophysiology")
- **Hallazgo citado:** "Hypopituitarism—particularly ACTH deficiency—is the most frequent and clinically relevant manifestation, as secondary adrenal insufficiency may be life-threatening if not promptly recognized and treated."
- **Usado en:** [[10-insuficiencia-suprarrenal-secundaria]]

### [REF-46] Pitfalls in the management of undiagnosed secondary adrenal insufficiency: a case report and review.
- **IDs:** PMID: 41776570 · PMCID: PMC13064267 · DOI: 10.1186/s13256-026-05924-0
- **Autores:** Sakai K, Yoshida T, Chiba T, Yamaga M, Takemoto M. · **Revista:** J Med Case Reports · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41776570
- **Tipo de evidencia:** case report + revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "secondary adrenal insufficiency hyponatremia normal potassium aldosterone")
- **Hallazgo citado:** "Prolonged cortisol deficiency in undiagnosed central adrenal insufficiency can lead to severe hypotonic hyponatremia due to inappropriate vasopressin secretion and malnutrition caused by inhibition of orexigenic signals."
- **Usado en:** [[10-insuficiencia-suprarrenal-secundaria]]

### [REF-47] Central Adrenal Insufficiency Unmasked After Pneumonia-Associated Asthma Exacerbation... Rathke's Cleft Cyst.
- **IDs:** PMID: 42147671 · PMCID: PMC13178710 · DOI: 10.7759/cureus.107114
- **Autores:** Yamamoto N, Ohta R, Yamasaki A, Sano C. · **Revista:** Cureus · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/42147671
- **Tipo de evidencia:** case report
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "secondary adrenal insufficiency hyponatremia normal potassium aldosterone")
- **Hallazgo citado:** "Persistent fatigue, hyponatremia, or neurological findings... should prompt evaluation for central adrenal insufficiency and pituitary pathology." (IS central da hiponatremia SIN la hiperpotasemia típica de la primaria)
- **Usado en:** [[10-insuficiencia-suprarrenal-secundaria]]

### [REF-48] Adrenal crises in adolescents and young adults.
- **IDs:** PMID: 35583847 · PMCID: PMC9242908 · DOI: 10.1007/s12020-022-03070-3
- **Autores:** Rushworth RL, Chrisp GL, Bownes S, Torpy DJ, Falhammar H. · **Revista:** Endocrine · **Año:** 2022 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/35583847
- **Tipo de evidencia:** revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: 'AUTH:"Rushworth" AND "adrenal crisis"')
- **Hallazgo citado:** "All patients with AI are at risk of AC, which have an estimated incidence of 6 to 8 ACs/100 patient years... precipitated by... physiological stress, such as an intercurrent infection."
- **Usado en:** [[01-insuficiencia-suprarrenal-primaria]]

### [REF-49] The Changing Epidemiology of Adrenal Insufficiency: Iatrogenic Factors Predominate.
- **IDs:** PMID: 36777466 · PMCID: PMC9909161 · DOI: 10.1210/jendso/bvad017
- **Autores:** Rushworth RL, Torpy DJ. · **Revista:** J Endocr Soc · **Año:** 2023 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/36777466
- **Tipo de evidencia:** cohorte epidemiológica
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: 'AUTH:"Rushworth" AND "adrenal crisis"')
- **Hallazgo citado:** "Secondary AI (SAI) admission rates increased by 91.7%, whereas admission rates for primary AI (PAI) remained unchanged."
- **Usado en:** [[10-insuficiencia-suprarrenal-secundaria]]

### [REF-50] Addisonian Crisis in a 39-Year-Old Woman With Primary Adrenal Insufficiency.
- **IDs:** PMID: 41853409 · PMCID: PMC12991911 · DOI: 10.7759/cureus.103607
- **Autores:** Itteera MR, Gutierrez M, Patel KH. · **Revista:** Cureus · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41853409
- **Tipo de evidencia:** case report
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "adrenal crisis gastrointestinal symptoms nausea vomiting hyponatremia presentation")
- **Hallazgo citado:** "presented with hypotension, bradycardia, and nausea secondary to an Addisonian crisis, likely precipitated by cyclic nausea and vomiting... leading to an inability to tolerate oral medication."
- **Usado en:** [[01-insuficiencia-suprarrenal-primaria]], [[04-causa-gi-h-pylori-obstruccion]]

### [REF-51] Isolated Adrenocorticotropin Deficiency With Depressive Symptoms.
- **IDs:** PMID: 41743173 · PMCID: PMC12930356 · DOI: 10.1210/jcemcr/luaf304
- **Autores:** Mikami K, Oiwa Y, Kometani M, et al. · **Revista:** JCEM Case Reports · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41743173
- **Tipo de evidencia:** case report
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "adrenal crisis gastrointestinal symptoms nausea vomiting hyponatremia presentation")
- **Hallazgo citado:** "Isolated adrenocorticotropin deficiency (IAD)... often presenting with nonspecific symptoms that can be misattributed to mental disorders or gastrointestinal diseases... persistent nausea, vomiting, anorexia... Intravenous hydrocortisone... led to a rapid improvement."
- **Usado en:** [[10-insuficiencia-suprarrenal-secundaria]], [[04-causa-gi-h-pylori-obstruccion]]

### [REF-52] Clinical manifestations and associated factors in acquired hypoaldosteronism in endocrinological practice.
- **IDs:** PMID: 36303866 · PMCID: PMC9592828 · DOI: 10.3389/fendo.2022.990148
- **Autores:** Ruiz-Sánchez JG, Calle-Pascual AL, Rubio-Herrera MÁ, De Miguel Novoa MP, Gómez-Hoyos E, Runkle I. · **Revista:** Frontiers in Endocrinology · **Año:** 2022 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/36303866
- **Tipo de evidencia:** cohorte (112 episodios, 86 pacientes)
- **Recuperado:** 2026-06-21 vía Europe PMC (search EXT_ID:36303866 — verificado en esta sesión)
- **Hallazgo citado:** "Reduced mineralocorticoid action can induce a decrease in urine K+ and H+ excretion and an increase in urine Na+ excretion, leading to hyperkalemia, and/or hyponatremia, often combined with metabolic acidosis... 94.6% cases showed hyperkalemia, 54.5% HH, and 60.3% MA."
- **Usado en:** [[01-insuficiencia-suprarrenal-primaria]], [[02-hiponatremia-hipovolemica-vomitos]]

### 🩸 VASCULAR / TROMBÓTICA

### [REF-53] Adrenal Hemorrhage: A Comprehensive Analysis of a Heterogeneous Entity.
- **IDs:** PMID: 38432745 · PMCID: PMC10917120 · DOI: 10.1016/j.mayocp.2023.10.002
- **Autores:** Dogra P, Chinthapalli M, Sandooja R, et al. · **Revista:** Mayo Clinic Proceedings · **Año:** 2024 · **Open Access:** no (abstract vía core)
- **URL:** https://europepmc.org/article/MED/38432745
- **Tipo de evidencia:** cohorte (n=363)
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "antiphospholipid syndrome adrenal insufficiency infarction")
- **Hallazgo citado:** "338 (93%) had unilateral AH and 25 (7%) had bilateral AH... Patients with bilateral AH were more likely to have underlying coagulopathy (44% vs 3%) and to develop primary adrenal insufficiency (72% vs 0%)."
- **Usado en:** [[12-hemorragia-infarto-suprarrenal-saf]]

### [REF-54] Adrenal Insufficiency Due to Adrenal Insult Following Acute Pancreatitis in a Child.
- **IDs:** PMID: 39935492 · PMCID: PMC11809432 · DOI: 10.1210/jcemcr/luaf025
- **Autores:** Sasidharan Pillai S, Robilliard R, Fredette ME, et al. · **Revista:** JCEM Case Reports · **Año:** 2025 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/39935492
- **Tipo de evidencia:** case report con seguimiento de imagen
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "antiphospholipid adrenal vein thrombosis Addison")
- **Hallazgo citado:** "The adrenal injury was attributed to ischemic injury... Magnetic resonance imaging... 8 months later showed diminutive adrenal glands with a marked decrease in size compared to the initial CT scan." (→ infarto → atrofia: reconcilia "suprarrenales pequeñas" con origen vascular antiguo)
- **Usado en:** [[12-hemorragia-infarto-suprarrenal-saf]]

### [REF-55] Adrenal involvement in antiphospholipid syndrome and SLE-spectrum disease: systematic review and pooled individual-patient analysis.
- **IDs:** PMID: 42317308 · PMCID: — · DOI: 10.3389/fimmu.2026.1851029
- **Autores:** Li SG, Long T, Yu R, et al. · **Revista:** Frontiers in Immunology · **Año:** 2026 · **Open Access:** no (abstract vía core)
- **URL:** https://europepmc.org/article/MED/42317308
- **Tipo de evidencia:** revisión sistemática + análisis IPD (n=155)
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "catastrophic antiphospholipid syndrome adrenal involvement")
- **Hallazgo citado:** "Hemorrhage-dominant adrenal injury was the leading imaging phenotype (66.9%), bilateral adrenal involvement was highly prevalent (86.3%)... adrenal insufficiency was the first manifestation in 73.6%... hyponatremia in 47/142 (33.1%), and hyperkalemia in 57/134 (42.5%)."
- **Usado en:** [[12-hemorragia-infarto-suprarrenal-saf]]

### [REF-56] Unusual case of antiphospholipid syndrome presenting as adrenal insufficiency.
- **IDs:** PMID: 32188612 · PMCID: PMC7078771 · DOI: 10.1136/bcr-2019-233631
- **Autores:** Warriach SA, Mustafa M, O'Keeffe D, Watts M. · **Revista:** BMJ Case Reports · **Año:** 2020 · **Open Access:** no (abstract vía core)
- **URL:** https://europepmc.org/article/MED/32188612
- **Tipo de evidencia:** case report
- **Recuperado:** 2026-06-21 vía Europe PMC (search EXT_ID:32188612 — verificado en esta sesión)
- **Hallazgo citado:** "the observed adrenal gland enlargement was secondary to bilateral adrenal infarction and haemorrhage... the subsequently observed marked reduction in adrenal gland size was not secondary to an assumed response to TB therapy, but rather the sequela of infracted atrophied adrenal glands, as a manifestation of the underlying antiphospholipid syndrome (APS)."
- **Usado en:** [[12-hemorragia-infarto-suprarrenal-saf]]

### [REF-57] Primary adrenal insufficiency due to bilateral adrenal hemorrhage-adrenal infarction in SLE and APS.
- **IDs:** PMID: 37436639 · PMCID: PMC10449959 · DOI: 10.1007/s42000-023-00463-5
- **Autores:** Bouki K, Venetsanaki V, Chrysoulaki M, et al. · **Revista:** Hormones (Athens) · **Año:** 2023 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/37436639
- **Tipo de evidencia:** case report + revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "antiphospholipid adrenal vein thrombosis Addison")
- **Hallazgo citado:** "Hyponatremia, hyperkalemia, hyperpigmentation, shock... highly suggestive of an acute adrenal crisis... bilateral adrenal vein thrombosis and subsequent hemorrhage can be part of the thromboembolic complications seen in... APS."
- **Usado en:** [[12-hemorragia-infarto-suprarrenal-saf]]

### [REF-58] Adrenal Hemorrhage in Patients with SLE and APS: A Case Report and Literature Review.
- **IDs:** PMID: 37794979 · PMCID: PMC10547568 · DOI: 10.1155/2023/6686168
- **Autores:** Jiang W, Chen D, Yang D, et al. · **Revista:** Int J Endocrinol · **Año:** 2023 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/37794979
- **Tipo de evidencia:** case report + revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "antiphospholipid adrenal vein thrombosis Addison")
- **Hallazgo citado:** "the importance of screening for adrenal insufficiency in patients with SLE or APS who present with abdominal complaints, asthenia, and hyponatremia. It is also recommended to test for APS all patients with adrenal hemorrhage."
- **Usado en:** [[12-hemorragia-infarto-suprarrenal-saf]]

### 💊 FARMACOLÓGICA / TÓXICA / IATROGÉNICA

### [REF-59] Drug-Induced Hyponatremia: Insights into Pharmacological Mechanisms and Clinical Practice Management.
- **IDs:** PMID: 41010788 · PMCID: PMC12471027 · DOI: 10.3390/jcm14186584
- **Autores:** Capinha M, Lavrador M, Liberato J, et al. · **Revista:** J Clin Med · **Año:** 2025 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41010788
- **Tipo de evidencia:** revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "drug-induced hyponatremia review mechanisms")
- **Hallazgo citado:** "Drug-induced hyponatremia... one of the most prevalent but frequently overlooked causes... drugs acting on digestive and locomotor systems, anti-infective drugs."
- **Usado en:** [[13-hiponatremia-farmacologica-iatrogenica]]

### [REF-60] Drug-Induced Hyponatremia Surveillance: A disproportionality analysis based on FAERS database.
- **IDs:** PMID: 42257098 · PMCID: PMC13238170 · DOI: 10.12669/pjms.42.4.13918
- **Autores:** Xi X, Bai Z, Liu S, Dong J. · **Revista:** Pak J Med Sci · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/42257098
- **Tipo de evidencia:** farmacovigilancia (FAERS)
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "proton pump inhibitor hyponatremia")
- **Hallazgo citado:** "Five drugs demonstrated the highest cases counts: furosemide (n=1,560), hydrochlorothiazide (n=1049), sertraline (n=899), omeprazole (n=864), citalopram (n=738)."
- **Usado en:** [[13-hiponatremia-farmacologica-iatrogenica]]

### [REF-61] SIADH is associated with different proton pump inhibitor use: a pharmacovigilance study.
- **IDs:** PMID: 35590283 · PMCID: PMC9121555 · DOI: 10.1186/s12882-022-02818-3
- **Autores:** Wang M, Zhang L, Jia M, et al. · **Revista:** BMC Nephrology · **Año:** 2022 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/35590283
- **Tipo de evidencia:** farmacovigilancia (FAERS)
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "proton pump inhibitor induced hyponatremia mechanism SIADH")
- **Hallazgo citado:** "273 reports of PPI-associated SIADH... The median time to SIADH onset was 22 (IQR 6-692) days after PPI administration."
- **Usado en:** [[13-hiponatremia-farmacologica-iatrogenica]]

### [REF-62] Proton Pump Inhibitors Induced Hyponatremia... The Role of Deprescribing.
- **IDs:** PMID: 40729144 · PMCID: PMC12225499 · DOI: 10.3390/reports7020033
- **Autores:** Marcianò G, Caroleo B, Catarisano L, et al. · **Revista:** Reports (MDPI) · **Año:** 2024 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/40729144
- **Tipo de evidencia:** case report + revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "omeprazole hyponatremia SIADH")
- **Hallazgo citado:** "Pantoprazole dismission induced an improvement in clinical symptoms and the normalization of sodium levels." (relación causal por retirada)
- **Usado en:** [[13-hiponatremia-farmacologica-iatrogenica]]

### [REF-63] Potomania and Beer Potomania: A Systematic Review of Published Case Reports.
- **IDs:** PMID: 40573123 · PMCID: PMC12196016 · DOI: 10.3390/nu17122012
- **Autores:** Micoanski KS, Soriano JM, Gozalbo MM. · **Revista:** Nutrients · **Año:** 2025 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/40573123
- **Tipo de evidencia:** revisión sistemática (44 casos)
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "excess water intake dilutional hyponatremia potomania")
- **Hallazgo citado:** "Potomania and beer potomania are rare but important causes of dilutional hyponatremia, resulting from excessive fluid intake combined with low solute consumption... Five cases developed osmotic demyelination syndrome due to rapid sodium correction."
- **Usado en:** [[13-hiponatremia-farmacologica-iatrogenica]], [[02-hiponatremia-hipovolemica-vomitos]]

### [REF-64] Intravenous Fluids in Hospitalized Patients: A Review of Best Practices.
- **IDs:** PMID: 41132472 · PMCID: PMC12543346 · DOI: —
- **Autores:** Wilson JL, Decker M, Cain C. · **Revista:** Missouri Medicine · **Año:** 2025 · **Open Access:** no
- **URL:** https://europepmc.org/article/MED/41132472
- **Tipo de evidencia:** revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "hypotonic fluids hospital-acquired hyponatremia")
- **Hallazgo citado:** "Hypertonic saline is used to rapidly correct severe acute hyponatremia, and hypotonic fluids are indicated for replacement of free water deficits... patient response should be closely monitored."
- **Usado en:** [[13-hiponatremia-farmacologica-iatrogenica]]

### [REF-65] Challenging cases of hyponatremia incorrectly interpreted by ChatGPT.
- **IDs:** PMID: 40405178 · PMCID: PMC12100905 · DOI: 10.1186/s12909-025-07235-2
- **Autores:** Berend K, Duits A, Gans ROB. · **Revista:** BMC Medical Education · **Año:** 2025 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/40405178
- **Tipo de evidencia:** estudio educativo / serie comentada
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "excess water intake dilutional hyponatremia potomania")
- **Hallazgo citado:** "Concurrent Addison's disease was correctly recognized in case 1 by ChatGPT in 2023 and 2024, whereas 81% of the clinicians missed this diagnosis."
- **Usado en:** [[01-insuficiencia-suprarrenal-primaria]]

### 🧠 FUNCIONAL / GI / OTROS

### [REF-66] Benign gastric outlet obstruction: evolving strategies from surgery to EUS-guided gastrojejunostomy.
- **IDs:** PMID: 41789393 · PMCID: PMC12957609 · DOI: 10.1177/26317745251398950
- **Autores:** Rizzo GEM, Infantino G, Rancatore G, et al. · **Revista:** Ther Adv Gastrointest Endosc · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41789393
- **Tipo de evidencia:** revisión
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "gastric outlet obstruction Helicobacter pylori peptic ulcer")
- **Hallazgo citado:** "Benign gastric outlet obstruction (bGOO)... etiologies ranging from peptic strictures to complex postsurgical or inflammatory conditions... Endoscopic balloon dilation shows excellent efficacy in simple peptic strictures."
- **Usado en:** [[04-causa-gi-h-pylori-obstruccion]]

### [REF-67] Endoscopic balloon dilation for peptic gastroduodenal stenosis with gastric outflow obstruction.
- **IDs:** PMID: 41535789 · PMCID: PMC12837236 · DOI: 10.1186/s12876-026-04619-6
- **Autores:** Zeyara A, Scarfone L, Jeremiasen M, et al. · **Revista:** BMC Gastroenterology · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41535789
- **Tipo de evidencia:** cohorte (n=58)
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "gastric outlet obstruction Helicobacter pylori peptic ulcer")
- **Hallazgo citado:** "Endoscopic balloon dilation was successful in 50 patients (86.2%)... Most patients with peptic stenosis causing gastric outflow obstruction can be treated successfully with endoscopic balloon dilation alone."
- **Usado en:** [[04-causa-gi-h-pylori-obstruccion]]

### [REF-68] [Cannabinoid Hyperemesis Syndrome: A Scoping Review].
- **IDs:** PMID: 41224199 · PMCID: — · DOI: 10.1055/a-2704-5465
- **Autores:** Bonnet U. · **Revista:** Fortschr Neurol Psychiatr · **Año:** 2025 · **Open Access:** no (abstract vía core)
- **URL:** https://europepmc.org/article/MED/41224199
- **Tipo de evidencia:** scoping review
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "cyclic vomiting syndrome adults diagnosis")
- **Hallazgo citado:** "cannabis-induced cyclic vomiting is now defined as cannabinoid hyperemesis syndrome (CHS)... Young adults are often affected... reliable differentiation... only possible by establishing remission during at least 6 months of abstinence... Hot showers and baths... can acutely alleviate the severe vomiting."
- **Usado en:** [[16-vomitos-ciclicos-cannabinoide]]

### [REF-69] Cannabinoid Hyperemesis Syndrome, 2016 to 2022.
- **IDs:** PMID: 41284293 · PMCID: PMC12645340 · DOI: 10.1001/jamanetworkopen.2025.45310
- **Autores:** Swartz JA, Franceschini D. · **Revista:** JAMA Network Open · **Año:** 2025 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41284293
- **Tipo de evidencia:** estudio transversal poblacional
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "cannabinoid hyperemesis syndrome")
- **Hallazgo citado:** "risk was highest at ages 18 to 25 years (RRR, 3.59...) and 26 to 35 years (RRR, 2.26...)."
- **Usado en:** [[16-vomitos-ciclicos-cannabinoide]]

### [REF-70] Avoidant-Restrictive Food Intake Disorder Is Common in Adults With Cyclic Vomiting Syndrome.
- **IDs:** PMID: 41923288 · PMCID: PMC13044328 · DOI: 10.1111/nmo.70294
- **Autores:** Venkatesan T, Goday PS, Arumugam S, et al. · **Revista:** Neurogastroenterol Motil · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41923288
- **Tipo de evidencia:** estudio prospectivo (n=80)
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "cyclic vomiting syndrome adults diagnosis")
- **Hallazgo citado:** "In cyclic vomiting syndrome (CVS), approximately 30% of patients remain symptomatic between episodes... at risk for ARFID were more likely to be malnourished (73% vs. 30%)... used cannabis more often."
- **Usado en:** [[16-vomitos-ciclicos-cannabinoide]]

### [REF-71] When Recurrent Pancreatitis Is Not Pancreatitis: Cyclic Vomiting Syndrome Masquerading as Acute Pancreatitis in a Young Adult.
- **IDs:** PMID: 41778006 · PMCID: PMC12951248 · DOI: 10.7759/cureus.102682
- **Autores:** Ottu Para NK, Kalakappara S, Abubacker MTM. · **Revista:** Cureus · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41778006
- **Tipo de evidencia:** case report
- **Recuperado:** 2026-06-21 vía Europe PMC (search, query: "cyclic vomiting syndrome adults diagnosis")
- **Hallazgo citado:** "a 20-year-old male... a highly stereotyped pattern... Upper gastrointestinal endoscopy... demonstrated proximal gastric congestion without erosions or ulceration... a classic four-phase cyclic pattern consistent with cyclic vomiting syndrome (CVS)."
- **Usado en:** [[16-vomitos-ciclicos-cannabinoide]]

---

> **3ª ronda (2026-06-22) — cierre etiológico hacia TB suprarrenal (REF-72 a REF-75).** Búsqueda dirigida a validar la hipótesis tuberculosa: criterios diagnósticos de TB suprarrenal (no exigen cultivo positivo), naturaleza paucibacilar (baciloscopia poco sensible), TB como causa histórica/líder de Addison, y micosis endémica latinoamericana como antagonista a no perder.

### 🦠 INFECCIOSA (3ª ronda — eje tuberculoso)

### [REF-72] Clinical characteristics of nine cases of adrenal tuberculosis and literature review.
- **IDs:** PMID: 41214357 · PMCID: PMC13194323 · DOI: 10.1007/s11255-025-04897-1
- **Autores:** Ye D, Gan N, Yang Y, Fei Z, Liu H, Liu X, Xia L. · **Revista:** International Urology and Nephrology · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/41214357
- **Tipo de evidencia:** serie de casos (n=9) + revisión de literatura (206 casos de 60 publicaciones)
- **Recuperado:** 2026-06-22 vía Europe PMC (search EXT_ID:41214357; query origen: "adrenal tuberculosis diagnosis difficulty negative culture biopsy paucibacillary")
- **Hallazgo citado:** "Adrenal tuberculosis predominantly affects both adrenal glands. Pathological findings are granulomatous inflammation and caseous necrosis. The diagnosis of adrenal tuberculosis relies on evidence of adrenal cortical insufficiency, extra-adrenal tuberculosis, laboratory confirmation of tuberculosis infection, characteristic imaging features, pathological examination, and diagnostic anti-tuberculosis therapy." · "Among 160 cases detailing treatment regimens, 152 cases (95%) underwent anti-tuberculosis therapy."
- **Usado en:** [[05-tuberculosis-sistemica]], [[01-insuficiencia-suprarrenal-primaria]]

### [REF-73] Optimizing pathological diagnosis of tuberculosis: qPCR outperforms acid-fast staining in formalin-fixed paraffin-embedded tissues and enables resistance profiling.
- **IDs:** PMID: 42040586 · PMCID: PMC13106081 · DOI: 10.3389/fmed.2026.1736555
- **Autores:** Hu Y, Liu P, Mei M, Quan C, Liu Q. · **Revista:** Frontiers in Medicine · **Año:** 2026 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/42040586
- **Tipo de evidencia:** estudio diagnóstico comparativo (n=1.050 muestras FFPE de inflamación granulomatosa)
- **Recuperado:** 2026-06-22 vía Europe PMC (search EXT_ID:42040586)
- **Hallazgo citado:** "qPCR demonstrated a higher positive rate compared to AFB staining (63.43% vs. 26.29%, p < 0.001)... exhibits high effectiveness in the pathological diagnosis of tuberculosis when culture methods are not feasible." → la **baja sensibilidad de la baciloscopia (~26%)** explica que un BAL con BAAR/PCR-TB negativos **no excluya** TB (enfermedad paucibacilar).
- **Usado en:** [[05-tuberculosis-sistemica]]

### [REF-74] Tuberculosis of the adrenal gland: a case report and review of the literature of infections of the adrenal gland.
- **IDs:** PMID: 25165474 · PMCID: PMC4138934 · DOI: 10.1155/2014/876037
- **Autores:** Upadhyay J, Sudhindra P, Abraham G, Trivedi N. · **Revista:** International Journal of Endocrinology · **Año:** 2014 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/25165474
- **Tipo de evidencia:** revisión + case report
- **Recuperado:** 2026-06-22 vía Europe PMC (search EXT_ID:25165474)
- **Hallazgo citado:** "Infections of the adrenal glands remain an important cause of adrenal insufficiency, especially in the developing world. Indeed, when Thomas Addison first described the condition that now bears his name over 150 years ago, the vast majority of cases were attributable to tuberculosis."
- **Usado en:** [[05-tuberculosis-sistemica]]

### [REF-75] Acute adrenal insufficiency due to paracoccidiodomycosis. Report of 2 cases.
- **IDs:** PMID: 32874849 · PMCID: PMC7452247 · DOI: 10.1016/j.mmcr.2020.08.001
- **Autores:** Motta JC, Barrera EC. · **Revista:** Medical Mycology Case Reports · **Año:** 2020 · **Open Access:** sí
- **URL:** https://europepmc.org/article/MED/32874849
- **Tipo de evidencia:** case report (2 casos)
- **Recuperado:** 2026-06-22 vía Europe PMC (search EXT_ID:32874849; query origen: "adrenal tuberculosis primary adrenal insufficiency Latin America South America cause")
- **Hallazgo citado:** "Paracoccidiodomycosis is an endemic infection in Latin America. It can affect several organs... We describe two cases of paracoccidiodomycosis presenting with Addison's disease... Antifungal management and hormone supplementation were given, achieving complete resolution of symptoms." → antagonista infeccioso latinoamericano que **se trata distinto** (antifúngico, no tuberculostáticos): a no perder hasta tener micología.
- **Usado en:** [[06-paracoccidioidomicosis]], [[05-tuberculosis-sistemica]]
