# Unbanked Population — Análisis Contramedidas Mining
**Fecha:** 2026-05-11 | **Metodología:** JTBD + CRT + TOC + Countermeasures + HDD | **Piloto:** Público (github.com/felipet1987/contramedidas-pilot)

## Resumen Ejecutivo

1,287 millones de adultos globally no pueden participar en la economía financiera formal. La barrera no es falta de fondos — 26% reporta documentación insuficiente como razón principal de exclusion. El sistema financiero está diseñado para quienes ya tienen acceso, y esa asunción embedded en cada layer hace que las alternativas sin cuenta bancaria sean possible but expensive and complex.

El sistema tiene 4 restricciones estructurales: payment infrastructure diseñada para banking, credit scoring que requiere historial formal (chicken-and-egg), savings informales sin protección institucional, e income informal no reconocible por sistemas formales.

Este análisis identifica 6 Quick Wins accionables por actores privados sin dependencia de intermediarios financieros regulados. La palanca primary: mobile money como on-ramp universal para pagos digitales.

---

## Contexto del Segmento

| Dato | Valor |
|------|-------|
| Adultos sin cuenta bancaria globally | 1,287 millones (21.3%) |
| En países de bajo ingreso | 53.6% unbanked |
| En África Subsahariana | 41.8% (~310M) |
| En MENA | 47.1% (~144M) |
| En LAC | 30.3% (~139M) |

**Razones de exclusion:**
- 51% — "no tiene suficiente dinero" (pero 26% dice que es documentación, no falta de fondos)
- 26% — documentación insuficiente
- 15% — no tiene confianza en bancos
- 13% — costo de cuenta muy alto

**Trabajos no resueltos (JTBDs):**
1. Gestionar dinero sin cuenta bancaria
2. Proteger ahorros de pérdida/robo
3. Acceder a crédito sin historial crediticio
4. Enviar dinero a familiares (remesas)
5. Evitar el ciclo de deuda cara
6. Transaccionar online sin cuenta bancaria
7. Proteger a la familia ante shocks sin seguro

---

## Current Reality Tree — Hallazgos clave

**Palanca primaria:** UDE-6-F-01 — 45% de unbanked en India tiene teléfono móvel mas no acceso a servicios financieros digitales.

**Palanca secundaria:** UDE-3-F-01 — 74% de crédito en África Subsahariana es informal.

**2 loops de refuerzo identificados:**

### Loop 1: Exclusión financiera auto-sostenida
```
Frustración digital → Menor acceso a oportunidades → Más dependencia de crédito informal → 
Tasas 5x más altas → Fear de deuda → Más ansiedad → Frustración digital (reinicia)
```

### Loop 2: Ahorro inseguro → Deuda cara
```
43% savings en casa → Anxiety por seguridad → Sin producto formal → 
ROSCA vulnerable → Shock requiere crédito informal → Tasas 5x más altas → Default → 
Menos ayuda disponible en próxima crisis → Savings en casa (reinicia)
```

---

## Estructura Sistémica y Modelos Mentales

### ESTs identificadas

| # | EST | Descripción |
|---|-----|-------------|
| EST-1 | Payment infrastructure para banking | Infraestructura de pagos diseñada para banking, no para personas. Asumciones embedded en cada layer. |
| EST-2 | Scoring crediticio chicken-and-egg | Para tener score necesitas history; para tener history necesitas access. Bootstrapping imposible. |
| EST-3 | Savings informales sin protección | ROSCA y cash existen porque no hay alternativa formal — pero no tienen protección institucional. |
| EST-4 | Income informal no reconocible | Freelancers y gig workers tienen income real pero volatility. Sistemas formales no pueden verify. |

### Modelos Mentales

| # | MM | Descripción |
|---|----|-------------|
| MM-1 | "Sin cuenta = no confiable" | Bank account = verification. Sin eso, counterparties no tienen manera de trust. |
| MM-2 | "Cash = único dinero real" | Efectivo es tangible, controlable. Dinero en cuenta es abstracto, propiedad del banco. |
| MM-3 | "Préstamo familiar es gratis" | Costo relacional y riesgo de shame no son visibles — pero existen y son altos. |
| MM-4 | "Sin cuenta = no trabajan suficiente" | Blame atribuido al individuo. Justifica inacción de policy makers y sector privado. |

---

## Countermeasures — Top Quick Wins

| Rank | QW | Causa | F | I | G | Total |
|------|-----|-------|---|---|---|-------|
| 1 | QW-01: Mobile Money On-Ramp | EST-1 | 5 | 4 | 4 | **13** |
| 2 | QW-04: Gig Work Payment via Mobile Money | EST-1+EST-4 | 5 | 3 | 4 | **12** |
| 3 | QW-02: Credit Scoring con Mobile Money History | EST-2 | 4 | 4 | 3 | **11** |
| 4 | QW-03: ROSCA Digital con Escrow | EST-3 | 4 | 3 | 4 | **11** |
| 5 | QW-MM-01: Campaign Cash tiene Costo Invisible | MM-2 | 5 | 2 | 2 | **9** |
| 6 | QW-MM-02: P2P Debt Refinancing Network | MM-3 | 3 | 3 | 1 | **7** |

### Roadmap de 3 fases

**Fase 1 — Flujo (<60 días):** QW-01 + QW-04
Proveer payment infrastructure básica que demuestre demanda real de pagos sin bank account.

**Fase 2 — Acceso (3-6 meses):** QW-02 + QW-03
Habilitar crédito y savings sobre la base de usuarios establecida en Fase 1.

**Fase 3 — Transformación (largo plazo):** QW-MM-01 + QW-MM-02
Cambiar Modelos Mentales. Impacto medido en años, no meses.

---

## Plan de Hipótesis (HDD)

| HYP | Validación | Invalidación |
|-----|-----------|-------------|
| HYP-QW01 (Mobile Money On-Ramp) | ≥50K transacciones + ≥500 usuarios en día 60 | <20K transacciones o <5% adopción |
| HYP-QW02 (Credit Scoring) | Score AUC ≥0.65 + ≥3 lenders integrando en 6 meses | Score AUC <0.55 o ningún lender a los 90 días |
| HYP-QW03 (ROSCA Digital) | ≥5 ROSCAs activas + ≥7/10 perceived security a día 60 | <3 ROSCAs a los 45 días o security <5/10 |
| HYP-QW04 (Gig Payment) | ≥$50K payroll + ≥10 empleadores en día 60 | <$20K payroll o >50% churn |

---

## Brechas y Límites

**Lo que este análisis no puede resolver:**

1. **KYC/identidad digital** — El onboarding sin bank account requiere verificar identidad de otra forma. Biometrics, phone number verification, o государственные IDs digitais son opciones, pero cada una tiene tradeoffs de privacy y regulación.

2. **Infraestructura de mobile money** — La integración con mobile money providers requiere partnership comercial. MNOs tienen leverage y pueden cobrar fees que makes the model less attractive.

3. **Regulación cambiaria** — En países con controles de capital, las remesas internacionales están reguladas. El modelo de payment sin bank account puede chocar con estas regulaciones.

4. **Adoption cultural** — Mover a personas de cash a digital requiere trust building que toma tiempo. Las campañas de awareness (QW-MM-01) son necessary but no sufficient.

5. **Scale sin capital** — Los modelos más prometedores (QW-01, QW-02) requieren capital para funcionar (integration costs, sales team). Sin funding, el ritmo de scaling es lento.

---

*Este documento es parte del pilot público de Contramedidas Mining. Los artefactos de cada fase están en github.com/felipet1987/contramedidas-pilot. La metodología completa está en github.com/felipet1987/contramedidas-mining.*
