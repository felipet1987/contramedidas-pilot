# TOC — Unbanked Population

## Input

CRT artifact (`cm-analysis/crt/unbanked-crt-2026-05-11.md`):
- Palanca primaria: UDE-6-F-01 (45% de unbanked tiene móvel mas no acesso a financial services)
- Palanca secundaria: UDE-3-F-01 (74% crédito en África Subsahariana es informal)
- Loop 1: Exclusión financiera auto-sostenida
- Loop 2: Ahorro inseguro → deuda cara → riesgo
- 4 ESTs, 4 MMs identificados

---

## Evaporating Cloud — Identificación del Conflicto Central

### Conflicto: Participate in digital economy vs. Maintain independence from banking system

```
     OBJETIVO COMÚN
           │
           ▼
    Necesidad: Participar en la ──► Prerrequisito A: Tener cuenta bancaria
    economía digital y proteger a la        (o producto financiero formal)
    familia ante shocks
           │
           │         ┌────────────────────────────┐
           │         │     CONFLICTO               │
           │         │ Bank account es el único      │
           │         │ path viable — pero requiere  │
           │         │ documentación, historial,     │
           │         │ y fees que este segmento    │
           │         │ no puede cumplir             │
           └────────►│                              ◄┘
                    Prerrequisito B: Mantener
                    autonomía sin depender de
                    intermediarios regulados
```

### Ramificación del conflicto

**Necesidad A:** Participar en la economía digital (pagos, remesas, trabajo freelance)
- **Prerrequisito A1:** Tener account bancaria
- **Prerrequisito A2:** Payment platforms acepten alternativa no-bancaria

**Necesidad B:** Proteger a la familia sin costo prohibitivo
- **Prerrequisito B1:** Acceso a savings sin fees
- **Prerrequisito B2:** Acceso a crédito sin collateral bank-dependent
- **Prerrequisito B3:** Protección ante shocks sin insurance formal

### Asunción central (inyección objetivo)

**Asunción:** "La única forma de participar en la economía financiera formal es a través de una cuenta bancaria."

Esta asunción es lo que hace que A y B sean mutuamente excluyentes. Si es falsa, el conflicto se disuelve.

**Inyección propuesta:** "Existe mecanismos de payment, savings, y crédito que operan fuera del sistema bancario formal y son accesibles para no-bancarios."

---

## Los 5 Pasos de Focalización

### Paso 1: Identificar la restricción

**Restricción principal:** Payment infrastructure diseñada para banking — no existe on-ramp no-bancaria para servicios financieros digitales básicos.

**Restricción secundaria:** Scoring models que requieren historial formal para crédito — imposibilitan bootstrapping.

### Paso 2: Explotar la restricción

Para la restricción principal (payment infrastructure):

- **Qué hacer:** Lever mobile money existente (M-Pesa, etc.) como on-ramp — ya tiene 56% penetration en Kenia entre unbanked
- **Cómo:** Vincular mobile money no a bank account, sino a identidad digital self-sovereign (ej: phone number + biometrics)
- **Evidencia:** M-Pesa procesa transacciones sin bank account — el modelo ya existe

Para la restricción secundaria (scoring):

- **Qué hacer:** Usar alternative data para credit scoring (mobile money history, payment patterns, gig income)
- **Cómo:** Partner con mobile money providers para usar transaction history como credit history proxy
- **Evidencia:** Branchless banking providers en Filipinas y Kenia ya usan mobile money history para micro-lending

### Paso 3: Subordinar todo lo demás

Las initiatives de savings y crédito deben subordinarse a la decisión de payment infrastructure:
- Si payment on-ramp existe, entonces savings products pueden vincularse a la misma account
- Si credit scoring usa alternative data, entonces lending puede ocurrir sin bank account

**Regla:** No desarrollar savings product isolated — debe leverage la payment infrastructure que ya existe.

### Paso 4: Elevar la restricción

**Para payment infrastructure:**
- Advocacy por regulaciones que requieran payment apps ofrezcan onboarding sin bank account (solo KYC telefónico o biométrico)
- Soporte técnico para que mobile money providers expandan servicios de pago

**Para scoring models:**
- Lobbying por marcos regulatorios que acepten alternative data para credit scoring
- Desarrollo de open-source credit scoring models basados en mobile money data

### Paso 5: Repetir

Una vez que payment infrastructure no-bancaria esté resuelta (restricción rompida):
- La nueva restricción será: Credit scoring para的人群 sin alternative data suficiente
- El ciclo se repite con la siguiente restricción emergente

---

## Análisis de Constrained vs. Unconstrained

| Área | Status | Impacto en UDEs |
|------|--------|---------------|
| Pagos digitalessin bank account | **CONSTRAINED** — primary constraint | Bloquea UDE-1-F-01, UDE-4-F-01, UDE-6-F-01, UDE-1-S-01 |
| Credit sin historial formal | **CONSTRAINED** — secondary constraint | Bloquea UDE-3-F-01, UDE-5-F-01, UDE-3-E-01, UDE-3-S-01 |
| Savings sin productos formales | **UNCONSTRAINED** — ROSCA y cash existen aunque imperfectamente | Afecta UDE-2-F-01 pero con workarounds |
| Remesas sin cuenta bancaria | **CONSTRAINED** — mercados formales cobran 6-7%, informales son riesgosos | Afecta UDE-4-F-01, UDE-4-S-01 |
| Shock protection sin seguro | **UNCONSTRAINED** — savings como self-insurance es la vía (aunque inadecuada) | Afecta UDE-7-F-01 pero es coping mechanism, no solución |

---

## Quick Wins priorizados

### QW-TOC-01: Mobile money como on-ramp universal
**Ataca:** Restricción principal — payment infrastructure sin bank account
**Basado en:** UDE-6-F-01, EST-1, META-01
**Modelo sin intermediario financiero:** Mobile money provider actúa como payment processor, no como custodian de funds (usuario mantiene ownership del money vía wallet self-custodied)
**F/I/G:** 5/5/4

### QW-TOC-02: Credit scoring basado en mobile money history
**Ataca:** Restricción secundaria — scoring sin historial formal
**Basado en:** UDE-3-F-01, EST-2, META-02
**Modelo sin intermediario financiero:** Algoritmo open-source que usa transaction history como proxy — no requiere bank account, solo acceso al phone
**F/I/G:** 4/4/3

### QW-TOC-03: ROSCA digital con tracking on-chain
**Ataca:** UDE-2-F-01, UDE-7-F-02
**Basado en:** EST-3, META-03
**Modelo sin intermediario financiero:** ROSCA que corre en una app simple donde el pool de funds se administra vía smart contract o escrowman confiable, sin custodian de plataforma
**F/I/G:** 4/3/4

---

## Gatecheck: ¿La restriction se movió?

Después de implementar QW-TOC-01 (mobile money on-ramp):
- El 45% de unbanked en India con móvil (UDE-6-F-01) obtiene acceso a payment services
- Pero todavía necesita identidad digital verificable (KYC)
- La próxima restricción: KYC requirements de payment platforms

**Conclusión:** La restricción se mueve de "payment infrastructure" a "KYC/identity verification". Repetir ciclo.
