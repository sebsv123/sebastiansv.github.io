# Supuestos y Plan de Validación — Kibbeh Halal Congelado
**SSV Advisory — Sebastián Sifontes Valentín** | **Fecha:** Marzo 2026 | **Confidencial**

> Este documento lista todos los supuestos del modelo financiero y operativo, con su rango de variación, impacto en el negocio y plan concreto de validación. Es un documento vivo: actualizar cuando se obtengan datos reales.

---

## ⚠️ Alerta Crítica de Inconsistencia Financiera

Antes de presentar el modelo a inversores, se requiere reconciliar la siguiente discrepancia:

- **`04_PL_mensual_36meses.csv`** (escenario Base) muestra EBITDA negativo en todos los 36 meses, siendo el más favorable el mes 36 con **-10.156€/mes**.
- **`06_Breakeven_Payback_IRR.csv`** declara break-even operativo en el **mes 18** y EBITDA total 36 meses de **-85.000€**.
- La suma del EBITDA mensual del P&L CSV en el escenario Base asciende a aproximadamente **-668.000€** acumulados en 36 meses, lo que es inconsistente con el -85.000€ del resumen.

**Causa probable**: diferente definición de OPEX o EBITDA entre ambos archivos, o distinto nivel de apalancamiento operativo considerado. El archivo `06` puede estar calculando EBITDA de contribución (sin OPEX fijo completo) mientras que el `04` incluye todos los costes.

**Acción requerida**: Revisar y reconciliar ambos modelos antes del siguiente pitch a inversores. Los números del `04_PL_mensual_36meses.csv` (granulares, mes a mes) son más fiables para el análisis de viabilidad.

---

## Tabla de Supuestos del Modelo

| # | Supuesto | Valor Base | Conservador | Agresivo | Impacto si Varía | Cómo Validar | Coste Validación | Tiempo | Prioridad |
|---|---|---|---|---|---|---|---|---|---|
| **PRECIOS Y MÁRGENES** | | | | | | | | | |
| 1 | Precio mayorista SKU1 (ternera 400g) | **2,80 €/bolsa** | 2,60 € | 3,00 € | ±0,20€/bolsa × 22.500 bolsas/mes (año 3) = ±4.500€/mes margen bruto | Validar con buyer DIA / Carrefour Express antes de fijar tarifa. Benchmark: croquetas premium (3,00-3,50€/400g), empanadillas (2,20-2,60€) | 0€ (reuniones comerciales) | 2-3 meses | 🔴 ALTA |
| 2 | PVP consumidor SKU1 | **4,20 €/bolsa** | 3,99 € | 4,50 € | Impacto en competitividad frente a tiendas étnicas (5-8€) y croquetas premium (3,50-4,50€) | Test de precio con panel de consumidores (n=50). Observación lineal en retail | 1.500-3.000€ (estudio consumidor) | 1 mes | 🟡 MEDIA |
| 3 | Margen retailer (markup aplicado) | **33%** (GPM) | 35% | 30% | ±1% markup = ±0,028€ impacto en PVP percibido | Negociación directa con buyer. Sector: 28-35% GPM en congelados | 0€ | 2 meses | 🔴 ALTA |
| **COGS FASE 1 (COPACKER)** | | | | | | | | | |
| 4 | Precio carne ternera halal (Fase 1+2) | **4,00 €/kg** | 4,50 €/kg | 3,70 €/kg | ±0,50€/kg sobre 180g/bolsa = ±0,09€/bolsa COGS | Solicitar cotización a 3 proveedores halal certificados (Argal Halal, El Pozo, Carnes Llorente) | 0€ | 2 semanas | 🔴 ALTA |
| 5 | Fee copacker (transformación) | **0,55 €/bolsa** | 0,70 €/bolsa | 0,45 €/bolsa | ±0,10€/bolsa = ±600€/mes en mes 6 (3.000 bolsas) | RFQ a 3 copacker halal certificados (IFS/BRC). Fee real varía por volumen mínimo y complejidad proceso | 0€ | 1 mes | 🔴 ALTA |
| 6 | Precio packaging doypack 400g (Fase 1) | **0,18 €/bolsa** | 0,22 €/bolsa | 0,16 €/bolsa | ±0,04€/bolsa en todos los volúmenes Fase 1 | Solicitar cotización a Coveris, Mondi, o proveedores de packaging flexible para pedidos mínimos (5.000-10.000 uds) | 0€ | 2 semanas | 🟡 MEDIA |
| 7 | Precio packaging doypack 400g (Fase 2) | **0,16 €/bolsa** | 0,18 €/bolsa | 0,14 €/bolsa | Economías de escala a >100.000 uds/año; negociar con proveedor | Contrato marco con proveedor de packaging para Fase 2. Cotizar >50.000 uds | 0€ | 1 mes (con Fase 2) | 🟢 BAJA |
| 8 | Merma del proceso productivo | **4%** sobre MP | 5% | 3% | ±1% merma: impacto directo en COGS (±0,04€/bolsa aprox.) | Ensayos de producción piloto con copacker. Mínimo 3 lotes de prueba | 3.000-5.000€ (coste materias primas piloto) | 2 meses | 🟡 MEDIA |
| 9 | Aceite fritura (consumo/bolsa) | **0,05 €/bolsa** | 0,07 €/bolsa | 0,04 €/bolsa | Impacto menor en COGS total | Medición real durante piloto de producción | 0€ (incluido en piloto) | Con piloto | 🟢 BAJA |
| **OPEX FASE 1** | | | | | | | | | |
| 10 | Fee base copacker (parte OPEX) | **8.000 €/mes** | 10.000 €/mes | 6.500 €/mes | ±1.500€/mes impacto directo en flujo de caja | Negociación contractual con copacker. Incluye: uso instalaciones, supervisión, utilities | 0€ | 1 mes | 🔴 ALTA |
| 11 | Coste logística congelada distribución (Fase 1) | **1.200 €/mes** | 2.000 €/mes | 900 €/mes | Variable con volumen de expediciones. Impacto en payback | Cotización a 2-3 operadores logísticos frío (ID Logistics, Frigoríficos Norte, Stef España) | 0€ | 2 semanas | 🟡 MEDIA |
| 12 | Almacenaje externo cámara congelados (Fase 1) | **800 €/mes** | 1.200 €/mes | 600 €/mes | Impacto en liquidez Fase 1 | Cotización a almacenes frigoríficos de la zona de producción | 0€ | 2 semanas | 🟡 MEDIA |
| 13 | Salario gerencia / fundador (Fase 1) | **2.000 €/mes** | 2.000 €/mes | 2.000 €/mes | Fijo; no varía | Decisión del fundador. Mínimo viable para sostenibilidad personal | 0€ | — | 🟢 BAJA |
| 14 | Marketing y trade marketing (Fase 1) | **2.000 €/mes** | 1.000 €/mes | 3.000 €/mes | Impacto en velocidad de adopción y rotación en retail. Más marketing → más ventas → mejora payback | Plan de marketing concreto con ROI por acción (coste degustación vs. incremento rotación) | 0€ | 1 mes | 🟡 MEDIA |
| **OPEX FASE 2** | | | | | | | | | |
| 15 | Alquiler nave industrial ~400m² | **3.200 €/mes** | 4.000 €/mes | 2.800 €/mes | ±500€/mes impacto directo. Varía mucho por zona geográfica | Búsqueda activa de naves en polígonos industriales de Madrid/Toledo/Guadalajara. Portales: Idealista Comercial, CBRE, BNP Paribas RE | 0€ | 1-2 meses | 🔴 ALTA |
| 16 | Energía eléctrica + gas (Fase 2, industrial) | **3.500 €/mes** | 5.000 €/mes | 2.800 €/mes | Alta sensibilidad al precio de la energía (0,18€/kWh supuesto vs. mercado real). ±1.000€/mes si sube precio energía | Cotización de tarifa industrial (>15 kW potencia) con 2-3 comercializadoras. Fijar precio con contrato anual | 0€ | 1 mes | 🟡 MEDIA |
| 17 | Salarios personal directo (3 operarios + jefe producción) | **9.600 €/mes** (sin SS) | 10.800 €/mes | 8.400 €/mes | ±600€/mes/operario. Depende de convenio colectivo (industria cárnica, Convenio FIAB) | Consultar Convenio Colectivo de la Industria de Elaboradores de Productos Cocinados (BOE). Calcular con SS (33%) | 0€ (consulta gratuita) | 2 semanas | 🟡 MEDIA |
| 18 | Amortización CAPEX Fase 2 (lineal 5 años) | **3.633 €/mes** | 3.633 €/mes | 3.633 €/mes | Fijo; depende del CAPEX real invertido | Verificar tras cierre de inversión y compra de maquinaria | 0€ | Mes 12-18 | 🟢 BAJA |
| **VOLÚMENES DE VENTA** | | | | | | | | | |
| 19 | Bolsas vendidas Mes 1 (Base) | **500 bolsas/mes** | 300 | 750 | Alta incertidumbre. Es el supuesto más crítico del modelo. Impacto cascada en todos los flujos | Validar con piloto en 10-20 tiendas durante 2-4 semanas antes del lanzamiento masivo. Benchmarks: productos similares en lanzamiento (croquetas nuevas SKU: 50-200 uds/tienda/mes) | 2.000-5.000€ (test piloto) | 1-2 meses | 🔴 ALTA |
| 20 | Bolsas vendidas Mes 6 (Base) | **3.000 bolsas/mes** | 1.800 | 4.500 | Determina necesidad real de working capital y fecha de lanzamiento Fase 2 | Registro de ventas reales. Revisión mensual de KPIs comerciales (sell-through, rotación) | 0€ (seguimiento operativo) | Mes 6 | 🔴 ALTA |
| 21 | Bolsas vendidas Año 2 media (Base) | **~8.000 bolsas/mes** | ~5.000 | ~12.000 | Punto crítico para decidir inicio Fase 2 (nave propia). Si <6.000/mes, retrasar Fase 2 | Revisión trimestral de ventas. Gate de decisión formal en Mes 9-10 | 0€ | Mes 10 | 🔴 ALTA |
| 22 | Bolsas vendidas Año 3 media (Base) | **~21.000 bolsas/mes** | ~13.000 | ~32.000 | Representa ~600M bolsas al año. Requiere distribución en +300 puntos de venta | Expansión progresiva de puntos de venta. Control de cuota de tienda | 0€ | Año 3 | 🟡 MEDIA |
| **MIX DE CANALES** | | | | | | | | | |
| 23 | Mix canal retail (% facturación) | **60%** | 50% | 70% | Retail tiene menor precio/bolsa pero mayor volumen. Si retail < 60%, ingresos se ven afectados negativamente | Negociaciones concretas con cadenas. El mix real depende de qué canales homologan el producto | 0€ | Mes 6-12 | 🟡 MEDIA |
| 24 | Mix canal horeca (% facturación) | **25%** | 20% | 30% | Horeca paga precio menor (SKU3 5,50€/kg = 2,20€/400g equiv.) pero mayor volumen por cliente | Red comercial horeca. Feria HORECA, ferias gastronómicas | 0€ | Mes 3-6 | 🟡 MEDIA |
| 25 | Mix canal étnico/especializado (% facturación) | **15%** | 10% | 20% | Canal de menor escala pero mayor precio (5-8€ PVP). Margen bruto potencialmente superior | Muestreo en tiendas halal de Madrid, Barcelona, Málaga | 0€ | Mes 1-3 | 🟢 BAJA |
| **PLAZOS Y CERTIFICACIONES** | | | | | | | | | |
| 26 | Plazo cobro retail (cuentas por cobrar) | **75 días** (media 60-90) | 90 días | 60 días | ±15 días × 28.000€/mes (mes 18) = ±14.000€ en circulante. Crítico para cash flow | Verificar en contrato marco con cada cadena. Mercadona: ≤30 días (ventaja). Carrefour/DIA: 60 días | 0€ (negociación contractual) | Mes 6-8 | 🔴 ALTA |
| 27 | Plazo obtención RGSEAA | **2-3 meses** | 4 meses | 1,5 meses | Retraso crítico en timeline. Si >4 meses: retrasa lanzamiento | Inicio inmediato tras constitución empresa. Contactar CCAA de la planta de producción | 1.200€ (ya incluido en CAPEX F1) | 2-3 meses | 🔴 ALTA |
| 28 | Plazo obtención certificación Halal | **2-3 meses** | 4 meses | 2 meses | Bloquea la venta del producto como "Halal". Sin certificación: producto no diferenciado | Solicitar auditoría inicial al Instituto Halal en el Mes 0. Tener copacker ya certificado en Fase 1 | 2.500€/año (ya incluido en CAPEX F1) | 2-3 meses | 🔴 ALTA |
| 29 | Plazo homologación primera cadena retail | **6-9 meses** | 12 meses | 4 meses | Retraso en primer pedido = retraso en ingresos y mayor consumo de working capital | Contacto con buyer DIA/Carrefour Express desde Mes 0 (antes de certificaciones). Presentación producto con muestras | 0€ (muestra física del producto) | 6-9 meses | 🔴 ALTA |
| **INFRAESTRUCTURA Y CAPEX** | | | | | | | | | |
| 30 | Coste adecuación nave industrial | **35.000 €** | 55.000 € | 25.000 € | ±20.000€ muy significativo. Varía por estado de la nave (obra nueva vs. nave ya acondicionada) | Visita y presupuesto de nave antes de firmar contrato de arrendamiento. Incluir cláusula de obra en contrato. Presupuesto de obra de reforma con 2 constructores | 0€ (presupuestos) | 1 mes (con firma nave) | 🔴 ALTA |
| 31 | Coste freidora industrial continua | **28.000 € (nueva)** / 16.000€ (2ª mano) | 32.000 € (nueva) | 16.000 € (2ª mano) | ±8.000€ en CAPEX F2. La 2ª mano reduce CAPEX pero incrementa riesgo de avería | Cotizar nueva: CFT Group, Florigo, Heat and Control. Cotizar 2ª mano: Surplex, BidSpotter | 0€ | 1-2 meses | 🟡 MEDIA |
| 32 | Coste formadora kibbeh automática | **22.000 € (nueva)** / 13.000€ (2ª mano) | 26.000 € | 13.000 € | ±6.000€ en CAPEX F2 | Cotizar: Handtmann, Stork, Mondini. 2ª mano: mismas plataformas | 0€ | 1-2 meses | 🟡 MEDIA |
| **OTROS** | | | | | | | | | |
| 33 | Coste logística congelada por pallet | **Incluido en OPEX 1.200€/mes** | 1.800 €/mes | 900 €/mes | Si se gestiona por pallet: estimado 50-80€/pallet para Madrid-Barcelona. Impacto escala con volumen | Cotización formal a Stef España, TDL, ID Logistics | 0€ | 2 semanas | 🟡 MEDIA |
| 34 | Rappel / bonificación a cadenas retail | **No incluido en modelo base** | 3% facturación anual | 1% | Si se incluye: 3% × 672.000€ (Año 3 base) = -20.160€ reducción ingresos netos | Incluir en negociación contractual. Presupuestar desde Año 2 | 0€ | Mes 8-12 (negociación) | 🟡 MEDIA |
| 35 | Descuento introductorio primer lanzamiento retail | **No modelizado** | -15% durante 3 meses | -10% | Si cadena exige descuento introductorio: reducción temporal del precio mayorista de 2,80€ a 2,38-2,52€ | Negociar con buyer. Incluir en modelo escenario de lanzamiento | 0€ | Mes 6-8 | 🟡 MEDIA |
| 36 | Número de puntos de venta (tiendas) al Mes 8 | **50 tiendas piloto** | 30 tiendas | 100 tiendas | Determina volumen mínimo facturable en el piloto. 50 tiendas × 150 bolsas/mes/tienda = 7.500 bolsas/mes (superior al base) | Negociación piloto regional con buyer DIA/Carrefour Express (Madrid/BCN) | 0€ | Mes 6-8 | 🔴 ALTA |
| 37 | Bolsas/tienda/mes en piloto (rotación) | **50-100 bolsas/tienda/mes** (hipótesis conservadora) | 30 | 150 | Determina si el piloto es suficiente para justificar expansión. <30 uds/tienda → riesgo de retirada del lineal | Seguimiento semanal de sell-through con el buyer. PLV y degustaciones en tienda para impulsar rotación | 1.500-3.000€ (promotoras) | Mes 8-12 | 🔴 ALTA |

---

## Resumen de Supuestos por Prioridad

### 🔴 ALTA PRIORIDAD (validar antes del primer pitch)

| # | Supuesto | Acción inmediata |
|---|---|---|
| 1 | Precio mayorista (2,80€) | Reunión con buyer DIA/Carrefour en los próximos 60 días |
| 4 | Precio carne ternera halal (4,00€/kg) | RFQ a 3 proveedores esta semana |
| 5 | Fee copacker (0,55€/bolsa) | RFQ a 3 copacker halal. Visita física |
| 10 | Fee base copacker OPEX (8.000€/mes) | Negociación contractual |
| 15 | Alquiler nave industrial (3.200€/mes) | Búsqueda activa en portales |
| 19 | Volumen ventas mes 1 (500 bolsas) | Test piloto o benchmark sector |
| 26 | Plazo cobro retail (75 días) | Verificar en contrato |
| 27 | Plazo RGSEAA (2-3 meses) | Iniciar trámite ya |
| 28 | Plazo certificación Halal (2-3 meses) | Solicitar auditoría inicial ya |
| 29 | Plazo homologación retail (6-9 meses) | Contacto buyer desde Mes 0 |
| 30 | Coste adecuación nave (35.000€) | Presupuesto antes de firmar |
| 36 | Nº tiendas piloto (50) | Negociar con buyer |

### 🟡 MEDIA PRIORIDAD (validar en primeros 3-6 meses)

Supuestos #2, #3, #6, #8, #11-14, #16-17, #23-25, #33-35, #37

### 🟢 BAJA PRIORIDAD (validar en Fase 2, mes 12+)

Supuestos #7, #9, #13, #18, #22, #25

---

## Nota sobre la Inconsistencia Financiera

El modelo muestra **tensiones financieras significativas** que deben explicarse claramente a los inversores:

1. **EBITDA negativo durante 36 meses** (escenario base en P&L detallado): El modelo proyecta que el negocio no genera EBITDA positivo en ningún mes dentro del horizonte de 36 meses según el `04_PL_mensual_36meses.csv`. Esto se debe a:
   - OPEX de Fase 2 muy elevado (42.781€/mes) frente a ingresos que crecen gradualmente
   - El punto de equilibrio EBITDA requiere >42.781€/0,52 margen = ~82.000€/mes de ingresos = ~29.000 bolsas/mes
   - En el escenario Base, se alcanzan ~22.500 bolsas/mes en el mes 36 — aún por debajo del break-even EBITDA

2. **Discrepancia con `06_Breakeven_Payback_IRR.csv`**: El archivo de métricas resumen indica break-even en mes 18, lo que es inconsistente con el P&L detallado. Esta discrepancia debe resolverse antes de presentar a inversores.

3. **Payback y IRR positivos**: Son posibles si la inversión se recupera mediante flujo de caja operativo (cobros - pagos variables) incluso con EBITDA negativo, o si hay un valor residual del negocio al año 3 que mejora el IRR.

**Recomendación**: Contratar a un CFO/asesor financiero para revisar y reconciliar el modelo antes del siguiente pitch.

---

*SSV Advisory — Sebastián Sifontes Valentín | Marzo 2026 | Confidencial*
*Versión 1.0 — Para uso interno y revisión por inversores acreditados bajo NDA*
