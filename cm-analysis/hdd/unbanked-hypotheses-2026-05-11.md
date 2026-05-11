# HDD — Unbanked Population (Hypotheses)

## Input

`cm-analysis/countermeasures/unbanked-qws-2026-05-11.md` (QWs)
`cm-analysis/research/unbanked-jtbd-2026-05-11.md` (JTBDs)

---

### HYP-QW01

**Hipótesis:**
"Creemos que crear una integration layer que conecta mobile apps a mobile money providers (M-Pesa, bKash, GCash) para permitir pagos digitales sin bank account resolverá [UDE-1-F-01: 1,287M de adultos no pueden recibir ni enviar pagos electrónicos sin efectivo físico o cuenta bancaria] para adultos de 18-55 años en países de bajo y lower-middle income que tienen teléfono móvil pero no cuenta bancaria porque el sistema financiero formal los exclude por requisitos de documentación. Lo anterior, porque EST-1 (payment infrastructure diseñada para banking) hace que la única vía de acceso sea a través de cuenta bancaria — y mobile money ya existe como alternativa técnica que no requiere bank account, solo falta integración accesible. Sabremos que tuvimos éxito cuando el volumen de transacciones digitales procesadas a través de la integration layer sea ≥50K transacciones/mes dentro de los primeros 90 días de operación en un mercado piloto."

**MVE (Mínimo Experimento Viable):**
- Duración: 60 días (mínimo para observar transactional patterns estacionales)
- Muestra mínima: 500 usuarios activos únicos que hicieron ≥1 transacción en el período (poder estadístico 80% para detectar adopción si tasa real ≥10%)
- Método: piloto controlado — una ciudad o región con alta penetración de mobile money pero baja adopción de payment digital
- Herramienta: analytics interno (transacciones por usuario, frecuencia, cantidad) + NPS survey vía WhatsApp

**Métricas leading (30–60 días):**
- Transacciones/mes: baseline 0 (producto nuevo) → target ≥50K
- Usuarios activos únicos: baseline 0 → target ≥500
- Tasa de adopción: baseline 0% → target >10% de usuarios registrados completan transacción

**Métricas lagging (90–180 días):**
- Tasa de retención a 90 días: baseline N/A → target >40% de usuarios hacen ≥2 transacciones
- Volumen de remesas procesadas: baseline 0 → target ≥$100K/mes en valor

**Umbral de validación:** ≥50K transacciones + ≥500 usuarios activos únicos en día 60.
**Umbral de invalidación:** <20K transacciones totales en día 60 O tasa de adopción <5% de usuarios registrados.

---

### HYP-QW02

**Hipótesis:**
"Creemos que utilizar mobile money transaction history como proxy para credit scoring resolverá [UDE-3-F-01: 74% de adultos en África Subsahariana que necesita crédito lo obtiene de fuentes informales] para adultos con ≥6 meses de transaction history en mobile money (≥20 transacciones documentadas) pero sin historial crediticio formal porque scoring models formales requieren historial en el sistema financiero que solo se construye accediendo al sistema — chicken-and-egg que impide a los no-bancarios construir el collateral que necesitarían. Lo anterior, porque EST-2 (scoring crediticio requiere historial formal) hace que la única forma de acceder a crédito formal sea having credit history, y mobile money transactions son evidencia objetiva de behavior financiero substitute. Sabremos que tuvimos éxito cuando al menos 3 MFIs o fintechs de lending adopten el score como input en su decisión de aprobación de crédito dentro de los primeros 6 meses post-launch."

**MVE:**
- Duración: 90 días (incluye onboarding de lenders + data collection window)
- Muestra mínima: 1,000 transaction histories anonimizadas para calibración + 3 lenders partners (poder estadístico para correlación si r≥0.3)
- Método: validación retrospectiva de score vs. actual repayment performance (si existe data histórica) + pilot con 1 MFI que aprueba crédito usando score como input
- Herramienta: open-source scoring engine (codebase) + dashboard para lenders

**Métricas leading (30–60 días):**
- Score accuracy: AUC ≥0.65 vs. actual repayment en dataset de validación
- Lenders que integran: baseline 0 → target ≥1 MFI
- Tiempo de onboarding lender: baseline N/A → target <2 semanas

**Métricas lagging (90–180 días):**
- Credit applications usando score: baseline 0 → target ≥100
- Approval rate con score: ≥30% (suficiente para validar que el score permite apopulation que hoy no califica)
- Default rate en loans aprobados con score: <10% (benchmark MFI industry)

**Umbral de validación:** Score AUC ≥0.65 Y ≥3 lenders integrando dentro de 6 meses.
**Umbral de invalidación:** Score AUC <0.55 O ningún lender Integrado a los 90 días.

---

### HYP-QW03

**Hipótesis:**
"Creemos que migrar ROSCAs existentes a una app con escrowman digital que protege el pool de funds resolverá [UDE-2-F-01: 43% de adultos en países de bajo ingreso guarda sus ahorros en casa o con family/friends] para participantes de ROSCAs existentes (≥3 ciclos completados, grupo de ≥6 miembros) en comunidades urbanas de bajos ingresos porque ROSCAs son el mecanismo informal más efectivo de savings que existe — pero son vulnerables a default del organizer o member dropout que destruye todo el savings acumulado. Lo anterior, porque EST-3 (savings informales sin protección institucional) hace que cuando una ROSCA falla, el participant lose todo el dinero ahorrado — un riesgo que nadie cuantifica ni mitiga. Sabremos que tuvimos éxito cuando ≥80% de participantes de ROSCAs migradas reporten en survey que se sienten más seguros con su savings que antes de usar la app, dentro de los primeros 90 días."

**MVE:**
- Duración: 60 días (1 ciclo ROSCA completo para validation)
- Muestra mínima: 50 participantes en 5 ROSCAs activas (≥5 miembros cada una) — sufficient para detectarse difference en perceived security si real effect ≥30%
- Método: migración de ROSCAs existentes a la app + survey pre/post con preguntas estandarizadas de perceived financial security
- Herramienta: in-app survey (5 preguntas Likert) + qualitative interviews (10 participantes)

**Métricas leading (30–60 días):**
- ROSCAs migradas: baseline 0 → target ≥5 groups activos
- Participantes activos: baseline 0 → target ≥50
- Completion rate de ciclo: baseline ~70% estimated en ROSCAs sin app → target ≥90%

**Métricas lagging (90–180 días):**
- Perceived security score: baseline estimated 4/10 → target ≥7/10
- Savings promedio por participante: baseline $50/mes (informal estimate) → target ≥$60/mes (más savings porque se sienten más seguros)
- Member dropout rate: baseline ~15% por ciclo → target <5%

**Umbral de validación:** ≥5 ROSCAs activas + ≥7/10 perceived security score a los 60 días.
**Umbral de invalidación:** <3 ROSCAs activas a los 45 días O perceived security <5/10.

---

### HYP-QW04

**Hipótesis:**
"Creemos que permitir a empleadores pagar wages directamente a mobile money wallets (sin bank account) resolverá [UDE-1-S-01: Exclusión de plataformas de trabajo freelance que pagan vía bank transfer] para gig workers y empleados informales con mobile money wallet activa en mercados donde empleadores formales requieren account bancaria para payroll porque la única barrera es que payroll systems no soportan mobile money como destino — no es que el employer no quiera pagar ni el worker no quiera recibir. Lo anterior, porque UDE-6-F-02 (empleadores requieren bank account para payroll) no es una restriction del mercado sino del infrastructure — la solución es un integration layer que hace la conversión de payroll → mobile money push. Sabremos que tuvimos éxito cuando ≥10 empleadores procesen ≥$50K en payroll через mobile money en los primeros 60 días post-launch."

**MVE:**
- Duración: 60 días (mínimo para 1-2 payroll cycles completos)
- Muestra mínima: 10 empleadores activos + 200 workers recibiendo pagos — sufficient para validar unit economics si employer retention ≥70%
- Método: piloto con empleadores existentes que ya pagan en cash y están dispuestos a cambiar
- Herramienta: employer dashboard analytics + worker satisfaction survey via WhatsApp

**Métricas leading (30–60 días):**
- Empleadores activos: baseline 0 → target ≥10
- Workers pagados: baseline 0 → target ≥200
- Payroll procesado: baseline 0 → target ≥$50K

**Métricas lagging (90–180 días):**
- Employer retention a 90 días: baseline N/A → target >80%
- Worker satisfaction: baseline N/A → target >8/10 NPS
- Tiempo de onboarding employer: baseline N/A → target <3 días

**Umbral de validación:** ≥$50K payroll procesado + ≥10 empleadores activos en día 60.
**Umbral de invalidación:** <$20K payroll a los 60 días O employer churn >50% en período.

---

## Dependencias entre hipótesis

| HYP | Puede correr cuando |
|-----|----------------------|
| HYP-QW01 | Puede lanzarse primero — no tiene dependencias |
| HYP-QW02 | Puede lanzarse en paralelo con HYP-QW01 — el scoring no depende de que payments funcione, pero se potencia si ya hay base de usuarios |
| HYP-QW03 | Puede lanzarse en paralelo — ROSCAs son independientes del payment infrastructure |
| HYP-QW04 | Debe esperar a que HYP-QW01 tenga traction (empleadores van a ask about payment capabilities primero) |

---

## Notas sobre invalidación

Todas las hipótesis tienen umbrales de invalidación definidos. Si una hipótesis invalidates:
1. No stop everything — cada QW tiene su propio validation criteria
2. El equipo decide: iterate on product, pivot approach, o abandons this particular QW y moves to next
3. Document what was learned — even failed experiments son valuable si se documentan correctamente

La única hipótesIs que, si invalidates, requeriría replantear todo el pilot es HYP-QW01 — porque si payment sin bank account no funciona, las demás hipótesis se built on una premisa incorrecta.
