# Business Plan — Kibbeh Congelado Premium | SSV Advisory
**Autor:** Sebastián Sifontes Valentín — SSV Advisory | **Fecha:** Marzo 2026 | **CONFIDENCIAL**

> Este repositorio contiene el Business Plan completo, el Data Room para inversores y la documentación técnica para la homologación retail del proyecto de kibbeh halal frito congelado para el mercado español.

---

## Índice Completo de Archivos

### 📁 `/business-plan/` — Documentos Principales

| Archivo | Descripción | Estado |
|---|---|---|
| [`BP_Kibbeh_España.md`](business-plan/BP_Kibbeh_España.md) | Business Plan completo — ~600 líneas. Estrategia, mercado, operaciones, marco regulatorio, plan financiero, riesgos, expansión UE | ✅ v2.0 Mar 2026 |
| [`investor_deck_outline.md`](business-plan/investor_deck_outline.md) | Investor Deck completo — 14 slides con contenido completo, cifras reales y notas para el presentador | ✅ v2.0 Mar 2026 |

---

### 📁 `/business-plan/financials/` — Modelos Financieros (Source of Truth)

> ⚠️ Los archivos CSV de esta carpeta son la **fuente de verdad** del modelo financiero. Todo el texto narrativo debe ser coherente con estos archivos.

| Archivo | Descripción | Cifra clave |
|---|---|---|
| [`01_CAPEX_detallado.csv`](business-plan/financials/01_CAPEX_detallado.csv) | CAPEX detallado por partida, Fase 1 y Fase 2 | Total: 320.000€ |
| [`02_OPEX_mensual.csv`](business-plan/financials/02_OPEX_mensual.csv) | OPEX mensual por partida, Fase 1 y Fase 2 | F1: 19.210€/mes / F2: 42.781€/mes |
| [`03_Unit_Economics.csv`](business-plan/financials/03_Unit_Economics.csv) | Unit economics por bolsa — COGS, márgenes, PVP | COGS F1: 1,82€ / F2: 1,35€ |
| [`04_PL_mensual_36meses.csv`](business-plan/financials/04_PL_mensual_36meses.csv) | P&L mensual 36 meses × 3 escenarios | Ver nota de consistencia abajo |
| [`05_Cashflow_mensual_36meses.csv`](business-plan/financials/05_Cashflow_mensual_36meses.csv) | Cashflow mensual 36 meses — cobros, pagos, saldo acumulado | — |
| [`06_Breakeven_Payback_IRR.csv`](business-plan/financials/06_Breakeven_Payback_IRR.csv) | Métricas resumen — Break-even, Payback, IRR, VAN por escenario | IRR: 22% (base) / Payback: 28m |

---

### 📁 `/business-plan/anexos/` — Documentación Técnica y Comercial

| Archivo | Descripción | Estado |
|---|---|---|
| [`checklist_APPCC.md`](business-plan/anexos/checklist_APPCC.md) | Sistema APPCC completo — PCCs, análisis de peligros, justificación PCCs, plan muestreo microbiológico, validación shelf life | ✅ v2.0 Mar 2026 |
| [`checklist_etiquetado.md`](business-plan/anexos/checklist_etiquetado.md) | Checklist etiquetado — conformidad Reglamento UE 1169/2011 | v1.0 Jun 2024 |
| [`checklist_homologacion_retail.md`](business-plan/anexos/checklist_homologacion_retail.md) | Homologación retail — requisitos comunes + específicos por cadena (DIA, Carrefour, ECI, Mercadona) | ✅ v2.0 Mar 2026 |
| [`especificacion_packaging.md`](business-plan/anexos/especificacion_packaging.md) | Especificaciones técnicas del packaging doypack | v1.0 Jun 2024 |
| [`ficha_tecnica_producto.md`](business-plan/anexos/ficha_tecnica_producto.md) | Ficha técnica completa SKU1 Ternera Halal 400g | v1.0 Jun 2024 |
| [`gantt_meses_0_12.csv`](business-plan/anexos/gantt_meses_0_12.csv) | Gantt de implementación meses 0-12 | v1.0 Jun 2024 |
| [`lista_maquinaria.md`](business-plan/anexos/lista_maquinaria.md) | Lista detallada de maquinaria para Fase 2 con precios de referencia | v1.0 Jun 2024 |
| [`one_pager_inversores.md`](business-plan/anexos/one_pager_inversores.md) | One-pager para primera toma de contacto — branding SSV Advisory, cifras actualizadas | ✅ v2.0 Mar 2026 |

---

### 📁 `/business-plan/deliverables/` — Data Room Investor-Ready

| Archivo | Descripción | Estado |
|---|---|---|
| [`README_deliverables.md`](business-plan/deliverables/README_deliverables.md) | Índice maestro del data room con guías de uso para inversores, retailers y reguladores | ✅ Mar 2026 |
| [`sources_master.md`](business-plan/deliverables/sources_master.md) | Tabla maestra de 40+ fuentes — todas las afirmaciones cuantitativas con enlace verificable o marcadas como SUPUESTO | ✅ Mar 2026 |
| [`assumptions_and_validation.md`](business-plan/deliverables/assumptions_and_validation.md) | Tabla de 37 supuestos — valor base, rango, impacto, cómo validar, coste y prioridad. Incluye alerta de inconsistencia financiera | ✅ Mar 2026 |
| [`investor_deck_SSV_Advisory.md`](business-plan/deliverables/investor_deck_SSV_Advisory.md) | Investor Deck completo — 14 slides con contenido completo, cifras reales, branding SSV Advisory | ✅ Mar 2026 |

---

## Cómo Usar los CSVs en Excel / Google Sheets

### Microsoft Excel

1. Abrir Excel → pestaña **Datos** → **Obtener datos** → **Desde texto/CSV**
2. Seleccionar el archivo CSV de la carpeta `business-plan/financials/`
3. En el asistente de importación:
   - **Separador**: Coma (`,`)
   - **Codificación**: UTF-8
   - **Primera fila como encabezado**: Activado
4. Hacer clic en **Cargar**
5. Para analizar un escenario: filtrar la columna `Escenario` con el valor deseado (Conservador / Base / Agresivo)

### Google Sheets

1. Abrir Google Sheets → **Archivo** → **Importar**
2. **Subir** → seleccionar el archivo CSV
3. Configuración de importación:
   - **Tipo de separador**: Coma
   - **Convertir texto a número, fecha, fórmula**: Activado
4. Hacer clic en **Importar datos**
5. Para tablas dinámicas: **Insertar** → **Tabla dinámica** → seleccionar rango de datos

### Consejo para el modelo consolidado

Para analizar todos los datos financieros juntos, importar los 6 CSVs en hojas separadas de un mismo libro de Excel/Sheets:
- Hoja 1: CAPEX (`01_CAPEX_detallado.csv`)
- Hoja 2: OPEX (`02_OPEX_mensual.csv`)
- Hoja 3: Unit Economics (`03_Unit_Economics.csv`)
- Hoja 4: P&L (`04_PL_mensual_36meses.csv`)
- Hoja 5: Cashflow (`05_Cashflow_mensual_36meses.csv`)
- Hoja 6: Métricas resumen (`06_Breakeven_Payback_IRR.csv`)

---

## Estructura del Data Room

```
📁 business-plan/
│
├── 📄 BP_Kibbeh_España.md              ← Business Plan completo (v2.0)
├── 📄 investor_deck_outline.md         ← Investor Deck 14 slides (v2.0)
│
├── 📁 financials/                      ← MODELOS FINANCIEROS (SOURCE OF TRUTH)
│   ├── 01_CAPEX_detallado.csv
│   ├── 02_OPEX_mensual.csv
│   ├── 03_Unit_Economics.csv
│   ├── 04_PL_mensual_36meses.csv
│   ├── 05_Cashflow_mensual_36meses.csv
│   └── 06_Breakeven_Payback_IRR.csv
│
├── 📁 anexos/                          ← DOCUMENTACIÓN TÉCNICA Y COMERCIAL
│   ├── checklist_APPCC.md              ← Sistema APPCC completo (v2.0)
│   ├── checklist_etiquetado.md
│   ├── checklist_homologacion_retail.md← Homologación retail (v2.0)
│   ├── especificacion_packaging.md
│   ├── ficha_tecnica_producto.md
│   ├── gantt_meses_0_12.csv
│   ├── lista_maquinaria.md
│   └── one_pager_inversores.md         ← One-pager inversores (v2.0)
│
└── 📁 deliverables/                    ← DATA ROOM INVESTOR-READY
    ├── README_deliverables.md          ← Índice data room
    ├── sources_master.md               ← Fuentes verificables
    ├── assumptions_and_validation.md   ← Supuestos y validación
    └── investor_deck_SSV_Advisory.md   ← Deck completo SSV Advisory
```

---

## Cifras Clave del Modelo

| Métrica | Valor | Fuente |
|---|---|---|
| Inversión total | **320.000€** | `01_CAPEX_detallado.csv` |
| COGS Fase 1 (copacker) | **1,82€/bolsa** | `03_Unit_Economics.csv` |
| COGS Fase 2 (nave propia) | **1,35€/bolsa** | `03_Unit_Economics.csv` |
| Margen bruto Fase 1 | **35%** | `03_Unit_Economics.csv` |
| Margen bruto Fase 2 | **52%** | `03_Unit_Economics.csv` |
| OPEX Fase 1 | **19.210€/mes** | `02_OPEX_mensual.csv` |
| OPEX Fase 2 | **42.781€/mes** | `02_OPEX_mensual.csv` |
| IRR 36 meses (Base) | **22%** | `06_Breakeven_Payback_IRR.csv` |
| Payback (Base) | **28 meses** | `06_Breakeven_Payback_IRR.csv` |
| VAN WACC 12% (Base) | **+62.000€** | `06_Breakeven_Payback_IRR.csv` |

---

## Disclaimer de Confidencialidad

> Este repositorio contiene información confidencial y propietaria de **SSV Advisory — Sebastián Sifontes Valentín**. Su acceso está restringido a inversores acreditados, compradores retail y asesores legales bajo NDA. Queda prohibida la distribución, reproducción o uso de esta información para fines distintos a la evaluación de la oportunidad de inversión descrita.
>
> Los datos marcados como **SUPUESTO** son estimaciones basadas en datos de mercado disponibles y conocimiento sectorial. No constituyen garantía de resultados futuros. La información financiera es proyectiva y sujeta a incertidumbre inherente a cualquier modelo de negocio en fase pre-revenue.
>
> Para el detalle completo de fuentes y validación de supuestos, ver:
> - [`business-plan/deliverables/sources_master.md`](business-plan/deliverables/sources_master.md)
> - [`business-plan/deliverables/assumptions_and_validation.md`](business-plan/deliverables/assumptions_and_validation.md)

---

**SSV Advisory — Sebastián Sifontes Valentín | Marzo 2026 | Confidencial**
