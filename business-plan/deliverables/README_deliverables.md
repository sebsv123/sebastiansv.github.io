# Data Room — Kibbeh Halal Congelado | SSV Advisory
**Autor:** Sebastián Sifontes Valentín — SSV Advisory | **Fecha:** Marzo 2026 | **Confidencial**

> Este directorio constituye el **Data Room** del proyecto Kibbeh para revisión por inversores y compradores retail. Todos los documentos están referenciados y enlazados desde este índice maestro.

---

## Índice del Data Room

### Carpeta raíz: `business-plan/`

| Archivo | Descripción | Estado | Versión |
|---|---|---|---|
| `BP_Kibbeh_España.md` | Business Plan completo (~600 líneas) — narrativa, estrategia, financiero, operaciones, compliance | ✅ Actualizado | 2.0 — Mar 2026 |
| `investor_deck_outline.md` | Investor Deck completo — 14 slides con contenido completo | ✅ Actualizado | 2.0 — Mar 2026 |

---

### Carpeta `financials/` — Modelos Financieros (Source of Truth)

> ⚠️ **Nota crítica**: Los archivos CSV de esta carpeta son la **fuente de verdad** del modelo financiero. Cualquier discrepancia entre el texto narrativo y los CSVs debe resolverse en favor de los CSVs.

| Archivo | Descripción | Hoja de cálculo |
|---|---|---|
| `01_CAPEX_detallado.csv` | CAPEX detallado por partida — Fase 1 (79.500€) y Fase 2 (218.000€) | Excel/Sheets: pestaña "CAPEX" |
| `02_OPEX_mensual.csv` | OPEX mensual por partida — Fase 1 (19.210€/mes) y Fase 2 (42.781€/mes) | Excel/Sheets: pestaña "OPEX" |
| `03_Unit_Economics.csv` | Unit economics por bolsa — COGS, márgenes, PVP. COGS F1: 1,82€ / F2: 1,35€ | Excel/Sheets: pestaña "Unit Econ." |
| `04_PL_mensual_36meses.csv` | P&L mensual 36 meses — 3 escenarios (Conservador/Base/Agresivo) | Excel/Sheets: pestaña "P&L" |
| `05_Cashflow_mensual_36meses.csv` | Cashflow mensual 36 meses — cobros, pagos, saldo acumulado | Excel/Sheets: pestaña "Cashflow" |
| `06_Breakeven_Payback_IRR.csv` | Métricas resumen — Break-even, Payback, IRR, VAN por escenario | Excel/Sheets: pestaña "Métricas" |

**Cómo usar los CSVs en Excel:**
1. Abrir Excel → Datos → Desde texto/CSV → seleccionar archivo
2. Delimitar por coma; encoding UTF-8
3. La primera fila es el encabezado

**Cómo usar en Google Sheets:**
1. Archivo → Importar → Subir → seleccionar CSV
2. Tipo de separador: Coma; Sin convertir texto a números (para conservar %)

---

### Carpeta `anexos/` — Documentación Técnica

| Archivo | Descripción | Estado |
|---|---|---|
| `checklist_APPCC.md` | Sistema APPCC completo — PCCs, análisis de peligros, registros, plan verificación | ✅ Actualizado v2.0 |
| `checklist_etiquetado.md` | Checklist etiquetado Reglamento UE 1169/2011 | ✅ v1.0 |
| `checklist_homologacion_retail.md` | Homologación proveedores retail — requisitos comunes y por cadena | ✅ Actualizado v2.0 |
| `especificacion_packaging.md` | Especificaciones técnicas del packaging doypack | ✅ v1.0 |
| `ficha_tecnica_producto.md` | Ficha técnica completa SKU1 Ternera Halal 400g | ✅ v1.0 |
| `gantt_meses_0_12.csv` | Gantt de implementación meses 0-12 | ✅ v1.0 |
| `lista_maquinaria.md` | Lista detallada de maquinaria para Fase 2 | ✅ v1.0 |
| `one_pager_inversores.md` | One-pager resumido para primera toma de contacto con inversores | ✅ Actualizado v2.0 |

---

### Carpeta `deliverables/` — Data Room Investor-Ready (este directorio)

| Archivo | Descripción | Estado |
|---|---|---|
| `README_deliverables.md` | **Este archivo** — índice maestro del data room | ✅ |
| `sources_master.md` | Tabla maestra de fuentes — todos los datos cuantitativos con enlace verificable o marcados como SUPUESTO | ✅ |
| `assumptions_and_validation.md` | Tabla de supuestos del modelo — valor, rango, impacto, cómo validar, prioridad | ✅ |
| `investor_deck_SSV_Advisory.md` | Investor Deck completo — 14 slides con contenido completo, branding SSV Advisory | ✅ |

---

## Guía de Uso del Data Room

### Para Inversores

1. **Primer contacto**: leer `one_pager_inversores.md` (5 min)
2. **Profundizar**: `investor_deck_SSV_Advisory.md` o `investor_deck_outline.md` (20 min)
3. **Due diligence financiero**: `financials/04_PL_mensual_36meses.csv` + `06_Breakeven_Payback_IRR.csv`
4. **Validar supuestos**: `deliverables/assumptions_and_validation.md`
5. **Verificar fuentes**: `deliverables/sources_master.md`
6. **Business Plan completo**: `BP_Kibbeh_España.md`

### Para Compradores Retail (KAMs / Buyers)

1. **Producto**: `anexos/ficha_tecnica_producto.md`
2. **Packaging**: `anexos/especificacion_packaging.md`
3. **Seguridad alimentaria**: `anexos/checklist_APPCC.md`
4. **Etiquetado**: `anexos/checklist_etiquetado.md`
5. **Proceso de homologación**: `anexos/checklist_homologacion_retail.md`

### Para Autoridades Regulatorias / Inspección

1. **APPCC**: `anexos/checklist_APPCC.md` — Sistema completo con PCCs y registros
2. **Etiquetado**: `anexos/checklist_etiquetado.md` — Conformidad Reglamento UE 1169/2011
3. **Ficha técnica**: `anexos/ficha_tecnica_producto.md`

---

## Estado General del Proyecto (Marzo 2026)

| Área | Estado | Próximo Paso |
|---|---|---|
| Constitución empresa | ⬜ Pendiente | Notaría + Registro Mercantil |
| RGSEAA | ⬜ Pendiente | Tramitar en CCAA de producción |
| Certificación Halal | ⬜ Pendiente | Contactar Instituto Halal / JAKIM |
| Copacker seleccionado | ⬜ En proceso | Due diligence 2 candidatos |
| Financiación | ⬜ En proceso | Presentación a inversores |
| Piloto retail | ⬜ Pendiente | Objetivo: DIA / Carrefour Express, 50 tiendas, Mes 8 |

---

## Disclaimer de Confidencialidad

> Este Data Room contiene información confidencial y propietaria de SSV Advisory — Sebastián Sifontes Valentín. Su acceso está restringido a inversores acreditados, compradores y asesores legales bajo NDA. Queda prohibida la distribución, reproducción o uso de esta información para fines distintos a la evaluación de la oportunidad de inversión descrita, sin autorización escrita expresa del autor.
>
> Los datos marcados como **SUPUESTO** son estimaciones basadas en datos de mercado disponibles y conocimiento sectorial. No constituyen garantía de resultados futuros. La información financiera es proyectiva y sujeta a incertidumbre.
>
> **SSV Advisory — Sebastián Sifontes Valentín | Marzo 2026**
