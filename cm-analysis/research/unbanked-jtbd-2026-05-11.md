# Research: Unbanked Population — JTBD Analysis
**Fecha:** 2026-05-11
**Modo:** EXISTING
**Fuente:** World Bank Global Findex Database 2025 (encuesta 2024); BIS Global Findex; ILO financial inclusion reports

## Contexto del segmento

### Definición operativa
Adultos (15+) sin cuenta en banco tradicional por requisitos de income verification, credit history, o documentación. No incluyen quienes eligen no tener cuenta.

### Magnitud global

| Dato | Valor | Fuente |
|------|-------|--------|
| Población global sin cuenta bancaria | ~1,287 millones (21.3% de adultos 15+) | World Bank Global Findex 2025 [1] |
| Sin cuenta en países de bajo ingreso | 53.6% | World Bank Global Findex 2025 [1] |
| Sin cuenta en países lower-middle income | 29.6% | World Bank Global Findex 2025 [1] |
| Sin cuenta en África Subsahariana | 41.8% (~310M) | World Bank Global Findex 2025 [1] |
| Sin cuenta en Medio Oriente y Norte de África | 47.1% (~144M) | World Bank Global Findex 2025 [1] |
| Sin cuenta en Latinoamerica y Caribe | 30.3% (~139M) | World Bank Global Findex 2025 [1] |

### Por qué no tienen cuenta (razones reportadas)

| Razón | % que reporta como razón principal |
|-------|----------------------------------|
| "No tiene suficiente dinero" | 51% | World Bank Findex 2025 [1] |
| "Documentos de identificación insuficientes" | 26% | World Bank Findex 2025 [1] |
| "No tiene confianza en bancos" | 15% | World Bank Findex 2025 [1] |
| "Familia ya tiene cuenta" | 14% | World Bank Findex 2025 [1] |
| "Costo de cuenta muy alto" | 13% | World Bank Findex 2025 [1] |
| "Lejanía geográfica" | 11% | World Bank Findex 2025 [1] |

### Comportamientos observables actuales (workarounds)

| Comportamiento | Descripción |
|----------------|-------------|
| Cash-based transactions | Todo en efectivo — pagas, cobranzas, ahorro en casa |
| Savings circles | tanda/arum/cajas de ahorro comunitarias informales |
| Mobile money (África) | M-Pesa y similares — 56% de kenianos sin cuenta usan mobile money [2] |
| ROSCA | Rotating savings and credit associations — ahorro grupal rotativo |
| Pawn shops | Empeño de bienes como fuente de crédito de emergencia |
| Employer advance | Anticipos de salario del empleador (sin formal banking) |
|榴 | Informal lending networks (family, friends, community) |

## JTBD 1: Gestionar dinero sin cuenta bancaria
**Job statement:** "Cuando necesito recibir, guardar, o enviar dinero sin una cuenta bancaria, quiero usar un método que no requiera una银行 ni documentos complejos, para poder participar en transacciones económicas básicas."
**Tipo core:** Funcional
**Barreras:**
- Ningún método universally available fuera del sistema bancario formal
- Mobile money requiere teléfono y cobertura, no universal
- Cash requiere físicamente transportarlo y guardarlo en casa (riesgo de robo/pérdida)
- ROSCA requiere grupo social pre-existente
**Evidencia:** 51% de unbanked reporta "no tiene suficiente dinero" como razón — pero 26% dice que es documentación, no falta de fondos. Esto sugiere que la barrera primary es acceso, no capacidad [1].

## JTBT 2: Proteger ahorros de pérdida o robo
**Job statement:** "Cuando guardo dinero en mi casa como único medio de ahorro, quiero que no se pierda por robo, incendio, o gasto impulsivo, para poder mantener un fondo de emergencia."
**Tipo core:** Funcional
**Barreras:**
- Cash en casa es vulnerable a robo y pérdida
- No hay institución que guarantee el ahorro
- Family members pueden tomar el dinero sin permiso (el hogar compartido es elunit de riesgo)
- Sin productos de ahorro informales accesibles en áreas rurales
**Evidencia:** En países de bajo ingreso, 43% de adultos con ahorros lo hace en casa o con family/friends [1].

## JTBD 3: Acceder a crédito sin historial crediticio
**Job statement:** "Cuando necesito dinero para una emergencia o oportunidad y no tengo historial crediticio, quiero poder pedir prestado sin que el banco me pida garantía ni history, para resolver la situación."
**Tipo core:** Funcional
**Barreras:**
- Scoring models requieren historial en el sistema formal — imposible bootstrapping
- Garantías exigidas por bancos tradicionales no disponibles para no-asset-holders
- Lenders informales cobran tasas extremadamente altas (100-300% anual en beberapa contextos)
- Microfinance institutions requieren group lending (peer pressure como collateral substitute)
**Evidencia:** En África Subsahariana, 74% de adultos con préstamo lo obtuvo de fuentes informales (family, friends, informal lender) [1].

## JTBD 4: Enviar dinero a familiares en otra ciudad o país
**Job statement:** "Cuando necesito enviar dinero a un familiar en otra ciudad o país, quiero un método que sea más rápido y barato que ir physically al punto de envío, para mantener la connection familiar."
**Tipo core:** Funcional
**Barreras:**
- Remittance formales (Western Union, banks) requieren cuenta en ambos extremos
- Transferencias de cash vía bus/conductores informales son el substitute actual
- Costos de remesa international promedian 6-7% del monto enviado [3]
- En zonas rurales, la distancia al punto de envío es barrera adicional
**Evidencia:** 30% de adultos en países en desarrollo envió dinero a otro país en 2024 [World Bank Findex]. Remittance costs promedio US$200: ~$12-14 por transferencia [3].

## JTBD 5: Evitar el ciclo de deuda cara
**Job statement:** "Cuando tengo una emergencia y no puedo acceder a crédito formal, quiero evitar caer en deudas con prestamistas informales que cobran intereses usurers, para no empeorar mi situación."
**Tipo core:** Funcional
**Barreras:**
- Prestamistas informales (casual lenders, shopkeepers) cobran 10-20% mensual en algunos mercados
- Una vez que se entra en default informal, es difícil salir y rebuildir access a crédito
- El shame associated con defaulting on family loans damages social capital
- No hay producto de consolidación de deuda informal
**Evidencia:** Households en países de bajo ingreso pagan tasas efectivas up to 5x más altas que hogares en países ricos por productos financieros comparables [BIS 2024].

## JTBD 6: Transaccionar online sin cuenta bancaria
**Job statement:** "Cuando quiero pagar algo online (servicios, bienes) o recibir pagos por trabajo remote, quiero hacerlo sin una cuenta bancaria, para poder participar en la economy digital."
**Tipo core:** Funcional
**Barreras:**
- La mayoría de payment gateways requieren linked bank account o credit card
- Platforms de trabajo freelance pagan a cuentas bancarias o PayPal (que también requiere bank account)
- Mobile money en algunos países puede vincularse a accounts de teléfonos pero la interoperabilidad es limitada
- KYC requirements de la mayoría de plataformas excluyen a quienes no tienen ID formal aceptado
**Evidencia:** En India, 45% de adultos sin cuenta bancaria tiene teléfono móvil — pero no puede usar la mayoría de financial services digital [BIS 2024].

## JTBD 7: Proteger a la familia ante shocks sin seguro
**Job statement:** "Cuando sucede una emergencia médica o pérdida de trabajo, quiero tener una forma de cubrir los costos sin tener que vender activos productivos ni pedir prestado a tasas abusivas, para proteger el wellbeing de mi familia."
**Tipo core:** Funcional
**Barreras:**
- Insurance products formales requieren bank account para pagar premiums
- Community insurance informales ( burial societies, tontines) existen pero coverage limitado
- Savings como self-insurance es el único mecanismo disponible para la mayoría de unbanked
- Gastos médicos son la causa #1 de empobrecimiento por gastos de salud en países de bajo ingreso [WHO]
**Evidencia:** 93% de gastos médicos en países de bajo ingreso son pagados out-of-pocket por households [WHO Global Health Expenditure]. Para un hogar unbanked sin savings, esto significa venta de activos o deuda.

## Meta-JTBD: Mantener dignidad financiera sin sistema formal
**Job statement:** "Cuando no puedo acceder a los servicios financieros que el sistema formal ofrece a quienes tienen historial y documentación, quiero encontrar我的 propias formas de participar en la economía y proteger a mi familia, para mantener mi autonomía y dignidad frente a un sistema que me excluye."
**Por qué es meta:** Unifica los 7 clusters anteriores bajo un tema de identidad y agency. El problema no es solo lack of financial services — es la exclusión de un sistema que presupone cosas (documentación, historial, cuentas) que una parte significativa de la población no puede cumplir. La respuesta es agency — encontrar o construir alternativas, no esperar a que el sistema formal cambie.
**Evidencia:** 26% de unbanked reporta que la barrera principal es documentación insuficiente — no funds. Esto es un problema de diseño del sistema, no del individuo. [1]

## Bibliografía

[1] World Bank Global Findex Database 2025 (encuesta 2024). https://www.worldbank.org/en/programs/financialinclusion/global-findex

[2] GSMA Mobile Money Database 2024. https://www.gsma.com/mobilemoney

[3] World Bank Remittance Prices Worldwide Database. https://remittanceprices.worldbank.org
