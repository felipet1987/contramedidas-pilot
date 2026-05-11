# Countermeasures — Unbanked Population (Quick Wins)

## Input

`cm-analysis/toc/unbanked-toc-2026-05-11.md` (TOC)
`cm-analysis/crt/unbanked-crt-2026-05-11.md` (ICE)

---

## QWs por EST

### QW-01 — Mobile Money On-Ramp sin Bank Account

**Causa raíz atacada:** EST-1 Sistemas de pago diseñados para banking — no hay on-ramp no-bancaria
**Modelo sin intermediario financiero:** Mobile money provider opera como payment processor, no custodian. Wallet self-custodied: usuario controla funds vía phone number + PIN. La plataforma no retiene float — solo cobra fee por transacción.

| Dimensión | Análisis |
|-----------|----------|
| **Técnica** | API USSD + app. Integración con mobile money provider existente (M-Pesa, bKash, GCash). KYC vía phone verification + biometric opcional. Tiempo: 3-4 meses para MVP. Stack: Node.js API + USSD gateway + mobile money SDK. |
| **Legal** | Sin licencia de intermediación financiera — provider es el PSP, no la app. La app es solo interface de acceso. Regulación: e-money license del central bank del país donde opera — pero esa licencia la tiene el mobile money provider, no la app. |
| **Económica** | B2B2C. Fee por transacción: 0.5-1% ( comparable a 6-7% de remesas formales). CAC: orgánica vía mobile money existing user base. Unit economics positivos desde mes 1 si volumen > 10K transacciones/mes. MRC: $2-5 por usuario activo. |

**UDEs que mueve:** UDE-1-F-01 (1,287M sin pagos digitales), UDE-4-F-01 (remesas 6-7%), UDE-6-F-01 (45% India con móvil sin acceso digital), UDE-1-S-01 (exclusión de freelance platforms)
**JTBD desbloqueado:** JTBD 1 (gestionar dinero sin cuenta), JTBD 4 (enviar dinero a familiares)
**Scores:** Factibilidad 5/5 · Impacto 4/5 · Ganancia 4/5 · **Total 13/15**

**Justificación de scores:**
- Factibilidad 5/5: M-Pesa ya existe y procesa transacciones sin bank account. La innovación es integration layer, no infraestructura nueva. Provider tiene licencia, app no necesita.
- Impacto 4/5: Ataca la restricción principal (payment infrastructure). Afecta 4 UDEs directos y el root cause de la economía digital exclusion.
- Ganancia 4/5: Transaction fees 0.5-1% son atractivos vs. 6-7% de remesas. Unit economics positivos rápido. Pero requiere integración con provider específico (limita escala).

---

### QW-02 — Credit Scoring con Mobile Money Transaction History

**Causa raíz atacada:** EST-2 Scoring crediticio requiere historial formal — bootstrapping imposible
**Modelo sin intermediario financiero:** Algoritmo open-source que usa mobile money transaction history como credit score proxy. El scoring corre localmente sobre data que el usuario autoriza compartir — no hay custodies de fondos ni productos de crédito emitidos por la plataforma.

| Dimensión | Análisis |
|-----------|----------|
| **Técnica** | Algoritmo: weighted transaction frequency + recency + amount patterns. Open-source. Integration vía API con mobile money providers que exponen transaction history con user consent. Output: credit score + recommendation engine. Stack: Python ML pipeline + REST API. MVP: 2 meses. |
| **Legal** | La plataforma genera un score, no presta dinero. No requiere licencia de intermediación financiera. El lending lo hacen institutions financieras tradicionales usando el score como input. Regulación: data privacy (GDPR/equivalente local) — consent es mandatory. |
| **Económica** | B2B SaaS. $0.50-2 por score generado, facturado a lender que usa el score. CAC: venta directa a MFIs y fintechs de lending. Si 10 lenders lo usan con 100K searches/mes → $50K-$200K MRR. Sin consumer-facing revenue. |

**UDEs que mueve:** UDE-3-F-01 (74% África crédito informal), UDE-5-F-01 (tasas 5x más altas), UDE-3-E-01 (shame deuda informal), UDE-3-S-01 (stigma default)
**JTBD desbloqueado:** JTBD 3 (acceder a crédito sin historial)
**Scores:** Factibilidad 4/5 · Impacto 4/5 · Ganancia 3/5 · **Total 11/15**

**Justificación de scores:**
- Factibilidad 4/5: Requiere partnership con mobile money provider para acceder a transaction data. Eso puede tardar. Pero el algoritmo es técnicamente simple (2 meses para MVP).
- Impacto 4/5: Si funciona, rompe el chicken-and-egg del credit scoring. Puede habilitando lending formal para poblaciones que hoy solo tienen opción informal.
- Ganancia 3/5: B2B con pricing basado en usage. Modelo validable pero requiere comercializarla a lenders. Menor potencial que QW-01.

---

### QW-03 — ROSCA Digital con Escrow Multipartidario

**Causa raíz atacada:** EST-3 Savings informales no tienen protección institucional — ROSCA vulnerable a default
**Modelo sin intermediario financiero:** ROSCA que corre en app donde el pool de funds se administra vía escrowman (notario digital o smart contract básico). Sin custodian de plataforma — el dinero fluye directamente de participantes a participantes en cada ciclo. El organizer de la ROSCA recibe fee por facilitar, no por administrar fondos.

| Dimensión | Análisis |
|-----------|----------|
| **Técnica** | App simple: crear ROSCA, invitar participantes, tracking de ciclos, notificaciones. Backend: escrow logic (sin smart contract — solo multi-signature authorization). Mobile-first. Stack: React Native + Firebase Auth + Stripe Connect (para multi-party split, no para custody). MVP: 6-8 semanas. |
| **Legal** | Contrato civil de servicios de coordinación entre participantes. La plataforma no custodia fondos — cobra fee de servicio (5-10% del pot). No requiere licencia financiera si el money no pasa por la plataforma. Legal opinion required por jurisdicción. |
| **Económica** | Fee de servicio: 5-10% del pot por ROSCA completada. Ejemplo: ROSCA de $100/miembro × 12 miembros = $1,200 pot. Platform fee: $60-120 por ROSCA. Si 100 ROSCAs activas/mes → $6K-$12K MRR. CAC: orgánica via network effects dentro de la app. |

**UDEs que mueve:** UDE-2-F-01 (43% savings en casa), UDE-2-E-01 (anxiety seguridad efectivo), UDE-7-F-02 (ROSCA vulnerable a default)
**JTBD desbloqueado:** JTBD 2 (proteger ahorros de pérdida/robo)
**Scores:** Factibilidad 4/5 · Impacto 3/5 · Ganancia 4/5 · **Total 11/15**

**Justificación de scores:**
- Factibilidad 4/5: App técnicamente simple. El challenge es adoption — ROSCAs existenten en comunidades pre-existentes, hay que migrarlas. Requiere trust building local.
- Impacto 3/5: Ataca un problema real (protección de savings) pero affecting primarily el mecanismo de savings, no el root cause de payment o credit. 3 UDEs directos.
- Ganancia 4/5: Fee por servicio genera revenue desde el primer ciclo. Unit economics claros. Pero la escala depende de network effects — puede ser lento.

---

### QW-04 — Gig Work Payment via Mobile Money Wallet

**Causa raíz atacada:** EST-1 + EST-4. Employer requiere bank account para payroll; income informal no reconocible.
**Modelo sin intermediario financiero:** Plataforma de gig work que paga directamente a mobile money wallet del trabajador. No requiere bank account ni PayPal. Employer paga a la plataforma en una sola transferencia; plataforma reparte a múltiples trabajadores vía mobile money push. Fee: 1-2% del total payroll procesado.

| Dimensión | Análisis |
|-----------|----------|
| **Técnica** | Dashboard employer (web) + payout to mobile money (API integration con MNO). Trabajador recibe notificación y acepta pago en su wallet. Stack: web dashboard + REST API + mobile money push API. MVP: 2 meses. |
| **Legal** | Employer es el pagador real — la plataforma es solo procesador de payroll. No hay custodies de fondos (employer transfiere a cuenta dedicada que se emptya diariamente hacia wallets). Fee facturado al employer, no al trabajador. Legal: pure B2B SaaS. |
| **Económica** | B2B SaaS: 1-2% del payroll total procesado. Employer típico con 50 workers × $500/pago quincenal = $50K payroll/mes → $500-$1K MRR por employer. CAC: sales directo a empleadores informales (hard). Si 20 empleadores → $10K-$20K MRR. |

**UDEs que mueve:** UDE-1-F-01, UDE-1-S-01 (exclusión freelance), UDE-6-F-02 (empleadores requieren bank account)
**JTBD desbloqueado:** JTBD 6 (transaccionar online sin cuenta bancaria)
**Scores:** Factibilidad 5/5 · Impacto 3/5 · Ganancia 4/5 · **Total 12/15**

**Justificación de scores:**
- Factibilidad 5/5: Técnicamente simple. Mobile money push API existe en la mayoría de MNOs. Employer paga payroll de todas formas — solo cambia el destino del pago.
- Impacto 3/5: Ataca employment exclusion pero no va al root cause (payment infrastructure). Limitado a gig workers con employers formales dispuestos a usarlo.
- Ganancia 4/5: B2B SaaS con pricing predecible y bajo churn (employer switching cost moderado). Pero el mercado total es menor que payment infrastructure.

---

## QWs por MM (Modelo Mental)

### QW-MM-01 — Campaign "Cash tiene costo invisible"

**Causa raíz atacada:** MM-2 "El efectivo físico es el único dinero real"
**Modelo sin intermediario financiero:** Campaña de awareness que muestra en términos concretos cuánto cuesta guardar savings en casa (robos, pérdida, riesgo familiar) vs. alternativas. Ejecutable via WhatsApp, radio comunitaria, SMS. Sin costo de distribución alto.

| Dimensión | Análisis |
|-----------|----------|
| **Técnica** | Content: videos cortos 30s + infographics + casos reales. Distribución: WhatsApp groups, radio comunitaria local, SMS con link. Métricas: views, shares, engagement. Budget: $500-$2K por campaign en un mercado. Tiempo: 1 mes de production. |
| **Legal** | No regulated. Pure awareness — no productos financieros involucrados. Sin licencias. |
| **Económica** | Nonprofit o social enterprise funding. Cost: $1K-$5K por mercado para launch. Revenue: N/A (si es nonprofit). Si es social enterprise → monetizable via brand partnerships o grants. |

**UDEs que mueve:** UDE-2-E-01 (anxiety efectivo), UDE-2-S-01 (efectivo vulnerable a uso no autorizado)
**JTBD desbloqueado:** JTBD 2 (proteger ahorros)
**Scores:** Factibilidad 5/5 · Impacto 2/5 · Ganancia 2/5 · **Total 9/15**

**Justificación de scores:**
- Factibilidad 5/5: No technical challenge. Solo content creation + distribución.
- Impacto 2/5: Cambiar Modelos Mentales toma meses o años. Campaign sola unlikely para mover needle significativamente.
- Ganancia 2/5: Si es nonprofit, no hay revenue model directo. Puede ser primer paso para trust-building con la comunidad.

---

### QW-MM-02 — P2P Debt Refinancing Network

**Causa raíz atacada:** MM-3 "Pedir prestado a la familia es gratis y sin riesgo"
**Modelo sin intermediario financiero:** Red P2P donde borrowers con deudas familiares costosas pueden encontrar lenders informales que cobran menos (parcialmente via network de trust pre-existente). La plataforma solo matchea y facilita el acuerdo — no toca money. Fee: flat $1-5 por match completado.

| Dimensión | Análisis |
|-----------|----------|
| **Técnica** | App simple: borrower ingresa su deuda (monto, tasa actual, reason), lender ingresa oferta (tasa, monto, condiciones). Algoritmo de match basado en network proximity y history. Contract templates disponibles (PDF). Mobile-first. Stack: React Native + backend. |
| **Legal** | La plataforma es marketplace de contactos — no presta dinero ni custodians funds. Fee por servicio de match. Contract templates son civiles. Legal opinion required para asegurar que no se está operando como broker financiero sin licencia. |
| **Económica** | Fee flat $1-5 por match completado. Si 100 matches/mes × $3 avg = $300 MRR. Muy bajo. Pero puede escalar via network effects. Revenue potencial si se cobra premium por verification o por histórico de repayment. |

**UDEs que mueve:** UDE-3-E-01 (shame deuda informal), UDE-3-S-01 (stigma default), UDE-5-F-01 (tasas 5x más altas)
**JTBD desbloqueado:** JTBD 5 (evitar ciclo de deuda cara)
**Scores:** Factibilidad 3/5 · Impacto 3/5 · Ganancia 1/5 · **Total 7/15**

**Justificación de scores:**
- Factibilidad 3/5: Requiere trust en la plataforma para compartir información financiera sensitive. Adoption puede ser lento.
- Impacto 3/5: Addressing el modelo mental incorrecto sobre debt familiar. Pero el problema más grande es access, no information asymmetry.
- Ganancia 1/5: Fee flat por match es muy bajo para generar revenue significativo. Solo viable como feature de otra plataforma, no como standalone.

---

## Tabla de ranking

| QW | Causa | F | I | G | Total | Fase |
|----|-------|---|---|---|-------|------|
| QW-01 | EST-1 | 5 | 4 | 4 | 13 | 1 |
| QW-04 | EST-1+EST-4 | 5 | 3 | 4 | 12 | 1 |
| QW-02 | EST-2 | 4 | 4 | 3 | 11 | 2 |
| QW-03 | EST-3 | 4 | 3 | 4 | 11 | 2 |
| QW-MM-01 | MM-2 | 5 | 2 | 2 | 9 | 3 |
| QW-MM-02 | MM-3 | 3 | 3 | 1 | 7 | 3 |

---

## Roadmap de 3 fases

### Fase 1 — Flujo (lanzable en <60 días)

**QWs:** QW-01 (mobile money on-ramp), QW-04 (gig work payment)
**Rationale:** Ambos解决的问题 es payment infrastructure — el problema más básico. Si funciona, habilita todo lo demás.

Goal: probar que hay demanda real de payment sin bank account. Métrica: transacciones procesadas > 1K en primer mes.

### Fase 2 — Acceso (lanzable en 3-6 meses)

**QWs:** QW-02 (credit scoring mobile money), QW-03 (ROSCA digital)
**Rationale:** Estos dependen de que QW-01 ya haya establecido base de usuarios. Credit scoring usa transaction history — necesita que la gente ya esté usando mobile money. ROSCA digital puede lançarse independientemente pero se potencia si ya hay base de usuarios con wallets.

Goal: credit scoring adoptado por al menos 1 MFI. ROSCA digital con >50 active groups.

### Fase 3 — Transformación (largo plazo, meses a años)

**QWs:** QW-MM-01 (awareness campaign), QW-MM-02 (P2P debt network)
**Rationale:** Modelos mentales no se cambian en meses. Estas iniciativas pueden empezar antes pero su impacto real se mide en años. Campaign puede empezar en paralelo a Fase 1; P2P debt puede esperar a tener base de usuarios.

Goal: measurable shift en survey de "percepción de savings sin bank account" — baseline vs. 12-month follow-up.
