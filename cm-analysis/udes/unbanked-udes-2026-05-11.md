# UDEs — Unbanked Population

## Cómo leer este documento

Cada UDE tiene:
- **ID**: identificación única
- **Enunciado**: hecho negativo presente y medible
- **Tipo**: Funcional (F), Emocional (E), Social (S), Meta (M)
- **Causas ←**: qué UDEs o factores externos lo producen
- **Efectos →**: qué UDEs están downstream
- **Evidencia**: dato o fuente que justifica la existencia del UDE

---

## UDEs Funcionales

### Core

### UDE-1-F-01
**Enunciado:** 1,287M de adultos no pueden recibir ni enviar pagos electrónicos sin efectivo físico o una cuenta bancaria, incluso cuando los montos son pequeños.
**Tipo:** Funcional
**Causas ←:** [Factor externo: sistemas de pago diseñados para clientes bancarios; sin cuenta no hay on-ramp]
**Efectos →:** UDE-1-E-01, UDE-6-F-01
**Evidencia:** 21.3% de adultos global (1,287M) no tiene cuenta bancaria [World Bank Findex 2025]

### UDE-2-F-01
**Enunciado:** 43% de adultos en países de bajo ingreso guarda sus ahorros en casa o con familia/amigos, con riesgo de robo, pérdida o gasto impulsivo no planificado.
**Tipo:** Funcional
**Causas ←:** [Factor externo: sin acceso a cuentas de ahorro formales, no hay producto diseñado para este segmento]
**Efectos →:** UDE-2-E-01
**Evidencia:** 43% de adultos con ahorros en países de bajo ingreso lo hace en casa o con family/friends [World Bank Findex 2025]

### UDE-3-F-01
**Enunciado:** 74% de adultos en África Subsahariana que necesita crédito lo obtiene de prestamistas informales (family, friends, informal lender), no de instituciones formales.
**Tipo:** Funcional
**Causas ←:** [Factor externo: scoring models requieren historial crediticio formal — bootstrapping imposible]
**Efectos →:** UDE-3-E-01, UDE-5-F-01
**Evidencia:** 74% de préstamos en África Subsahariana son de fuentes informales [World Bank Findex 2025]

### UDE-4-F-01
**Enunciado:** El costo promedio de envío de remesas internationales 6-7% del monto enviado (US$12-14 por cada US$200 transferidos), sin opción barata sin cuenta bancaria.
**Tipo:** Funcional
**Causas ←:** [Factor externo: mercado de remesas dominado por operadores formales que cobran por acceso; 30% de adultos en países en desarrollo envió dinero a otro país en 2024]
**Efectos →:** UDE-4-E-01
**Evidencia:** Costos de remesa 6-7% promedio global; 30% de adultos envió dinero cross-border [World Bank Findex 2025, Remittance Prices Database]

### UDE-5-F-01
**Enunciado:** Hogares en países de bajo ingreso pagan tasas efectivas hasta 5x más altas que hogares en países ricos por productos financieros comparables debido a su condición de no-bancarios.
**Tipo:** Funcional
**Causas ←:** UDE-3-F-01
**Efectos →:** UDE-5-E-01
**Evidencia:** Hogares en países de bajo ingreso pagan hasta 5x más por crédito equivalente [BIS 2024]

### UDE-6-F-01
**Enunciado:** 45% de adultos sin cuenta bancaria en India tiene teléfono móvil pero no puede usar la mayoría de servicios financieros digitales por falta de account linking.
**Tipo:** Funcional
**Causas ←:** [Factor externo: KYC requirements y account-linking de payment platforms diseñados para clientes bancarios]
**Efectos →:** UDE-6-E-01, UDE-6-S-01
**Evidencia:** 45% de unbanked en India tiene móvil pero no acceso a financial services digital [BIS 2024]

### UDE-7-F-01
**Enunciado:** 93% de gastos médicos en países de bajo ingreso son pagados out-of-pocket por households, sin mecanismo de pooling ni seguro.
**Tipo:** Funcional
**Causas ←:** [Factor externo: productos de seguro formales requieren bank account para premiums; community insurance informal tiene coverage limitado]
**Efectos →:** UDE-7-E-01
**Evidencia:** 93% de gasto médico en países de bajo ingreso es out-of-pocket [WHO Global Health Expenditure]

### Supporting

### UDE-1-F-02
**Enunciado:** Mobile money (M-Pesa y otros) requiere teléfono y cobertura de red, pero 11% reporta lejanía geográfica como barrera — misma barrera que para banca tradicional.
**Tipo:** Funcional (Supporting — JTBD 1)
**Causas ←:** [Factor externo: infraestructura de telecomunicaciones no cubre todas las áreas rurales]
**Efectos →:** UDE-1-F-01
**Evidencia:** 56% de kenianos sin cuenta bancaria usa mobile money [GSMA 2024]; 11% menciona distancia geográfica [World Bank Findex 2025]

### UDE-3-F-02
**Enunciado:** Microfinance institutions requieren group lending como substitute de collateral, pero esto impone peer pressure y riesgo social sobre personas ya vulnerables.
**Tipo:** Funcional (Supporting — JTBD 3)
**Causas ←:** [Factor externo: productos MFIs diseñados para funcionar con group liability en vez de credit history]
**Efectos →:** UDE-3-F-01
**Evidencia:** MFIs existen masivamente en mercados no-bancarios con modelo group lending [World Bank Findex 2025]

### UDE-4-F-02
**Enunciado:** Transferencias de efectivo vía bus/conductores informales son el mecanismo substitute para quienes no tienen cuenta — sin garantía de entrega ni protección contra fraude.
**Tipo:** Funcional (Supporting — JTBD 4)
**Causas ←:** UDE-4-F-01
**Efectos →:** UDE-4-E-01
**Evidencia:** Mercado informal de remesas existe donde formales no llegan — práctica común en zonas rurales de África y Asia [observación documented in World Bank research]

### UDE-7-F-02
**Enunciado:** ROSCA ( Rotating Savings and Credit Associations) son el mecanismo informal más extendido de ahorro y crédito grupal, pero requieren grupo social pre-existente y tienen riesgo de default no recoverable.
**Tipo:** Funcional (Supporting — JTBD 7)
**Causas ←:** UDE-2-F-01
**Efectos →:** UDE-7-E-01
**Evidencia:** ROSCA/tanda/arum son mecanismos documentados en >40 países como sistema informal de ahorro rotativo [BFII, ILO]

---

## UDEs Emocionales

### Core

### UDE-1-E-01
**Enunciado:** Incapacidad de participar en transacciones digitales básicas genera frustración y sensación de incompetencia frente a un mundo que asume que todos tienen acceso a banking.
**Tipo:** Emocional
**Causas ←:** UDE-1-F-01
**Efectos →:** UDE-META-E-01
**Evidencia:** [inferido — la frustración de la exclusión digital es ampliamente documentada en estudios de financial inclusion]

### UDE-2-E-01
**Enunciado:** Ansiedad persistente por la seguridad del efectivo guardado en casa — miedo constante a robo, incendio, o que alguien de la familia lo gaste sin permiso.
**Tipo:** Emocional
**Causas ←:** UDE-2-F-01
**Efectos →:** UDE-META-E-01
**Evidencia:** [inferido — el anxiety por savings insecurity es correlato documented del stress financiero en hogares no-bancarios]

### UDE-3-E-01
**Enunciado:** Vergüenza de pedir prestado a familiares y amigos, y anxiety por no poder devolver — el shame de la deuda informal daña relationships y el self-worth.
**Tipo:** Emocional
**Causas ←:** UDE-3-F-01
**Efectos →:** UDE-META-E-01
**Evidencia:** [inferido — deuda informal familiar tiene social stigma documentado en estudios de household finance en mercados emergentes]

### UDE-4-E-01
**Enunciado:** Anxiety sobre si la remesa llegará a tiempo cuando un familiar tiene una emergencia — sin tracking ni guarantee, la incertidumbre es constante.
**Tipo:** Emocional
**Causas ←:** UDE-4-F-01
**Efectos →:** UDE-META-E-01
**Evidencia:** [inferido — ansiedad por delivery guarantee de remesas es correlato conocido de la exclusion financiera]

### UDE-5-E-01
**Enunciado:** Fear de caer en espiral de deuda que no se puede salir — una vez en default informal, es casi imposible rebuildir acceso a crédito por años.
**Tipo:** Emocional
**Causas ←:** UDE-5-F-01
**Efectos →:** UDE-META-E-01
**Evidencia:** [inferido — debt spiral anxiety es ampliamente reportada en poblaciones sin acceso a crédito formal]

### UDE-6-E-01
**Enunciado:** Sentimiento de obsolescencia frente a un mundo que se数字化a — la economía digital avanza y ellos quedan atrás sin poder participar.
**Tipo:** Emocional
**Causas ←:** UDE-6-F-01
**Efectos →:** UDE-META-E-01
**Evidencia:** [inferido — digital exclusion produce documented feelings de left-behind en poblaciones no-bancarias]

### UDE-7-E-01
**Enunciado:** Fear permanente de un shock (médico, pérdida de trabajo) sin red de protección — el único amortiguador es el ahorro en efectivo guardado en casa (UDE-2-F-01), lo cual a su vez genera anxiety (UDE-2-E-01).
**Tipo:** Emocional
**Causas ←:** UDE-7-F-01
**Efectos →:** UDE-META-E-01
**Evidencia:** [inferido — health shock anxiety es componente central del financial stress en hogares sin seguro]

### Supporting

### UDE-7-E-02
**Enunciado:** Cuando un hogar cae en deuda médica o de emergencia, el stress financial se convierte en conflicto doméstico y afecta la salud mental de todos los miembros.
**Tipo:** Emocional (Supporting — JTBD 7)
**Causas ←:** UDE-7-F-01
**Efectos →:** UDE-7-E-01
**Evidencia:** [inferido — household financial stress correlaciona con conflicto doméstico documentado en estudios de salud pública]

---

## UDEs Sociales

### Core

### UDE-1-S-01
**Enunciado:** Exclusión de plataformas de trabajo freelance (Upwork, Fiverr, Freelancer) que pagan vía PayPal o bank transfer — el trabajo remote no está disponible sin cuenta bancaria.
**Tipo:** Social
**Causas ←:** UDE-6-F-01, UDE-1-F-01
**Efectos →:** UDE-META-S-01
**Evidencia:** [inferido — plataformas de trabajo freelance global requieren bank account o PayPal (que requiere bank account) para payout]

### UDE-2-S-01
**Enunciado:** Family members toman dinero del hogar sin consulta — el efectivo físico es vulnerable a uso no autorizado por cualquier persona del hogar, generando conflictos domésticos.
**Tipo:** Social
**Causas ←:** UDE-2-F-01
**Efectos →:** UDE-META-S-01
**Evidencia:** [inferido — efectivo compartido en hogar es source documentado de conflicto y lack of individual financial autonomy]

### UDE-3-S-01
**Enunciado:** Default en deuda informal con prestamista o family member daña el capital social — en comunidades pequeñas, el default se conoce públicamente y cierra futuras fuentes de ayuda.
**Tipo:** Social
**Causas ←:** UDE-3-F-01, UDE-5-F-01
**Efectos →:** UDE-META-S-01
**Evidencia:** [inferido — social capital loss por default es mecanismo ampliamente documentado en literatures de microcredit y community finance]

### UDE-4-S-01
**Enunciado:** La familia extendida depende de que las remesas lleguen — si el costo de envío es alto, se envía menos o se deja de enviar, dañando relationships familiares.
**Tipo:** Social
**Causas ←:** UDE-4-F-01
**Efectos →:** UDE-META-S-01
**Evidencia:** [inferido — remittances son lifeline financiero para familias en países en desarrollo; alto costo reduce monto enviado y frecuencia]

### UDE-5-S-01
**Enunciado:** En comunidades donde todos se conocen, ser known as alguien en debt con prestamistas informales cierra oportunidades — nadie quiere business relationship con alguien en situación de insolvency visible.
**Tipo:** Social
**Causas ←:** UDE-5-F-01
**Efectos →:** UDE-META-S-01
**Evidencia:** [inferido — stigma de debt en comunidades small/tradicionales es mecanismo conocido de perpetuación de pobreza]

### UDE-6-S-01
**Enunciado:** La exclusión de la economía digital amplifica inequality existente — quienes no pueden participar pierden acceso a mejores precios, mercados, y oportunidades de income.
**Tipo:** Social
**Causas ←:** UDE-6-F-01
**Efectos →:** UDE-META-S-01
**Evidencia:** [inferido — digital divide como amplifier de inequality económica es ampliamente documentado]

### UDE-7-S-01
**Enunciado:** Cuando un hogar no puede cubrir gastos médicos, los hijos son los primeros受影响 — ausentismo escolar, trabajo infantil, nutrición insuficiente como consecuencias observables del shock financiero.
**Tipo:** Social
**Causas ←:** UDE-7-F-01
**Efectos →:** UDE-META-S-01
**Evidencia:** [inferido — medical household financial stress produce outcomes documentados en niños: ausentismo escolar, trabajo infantil]

### Supporting

### UDE-6-S-02
**Enunciado:** Employers prefieren contratar personal con account bancaria para pagarles (más fácil para payroll), dejando a los no-bancarios fuera de trabajos formales even when qualified.
**Tipo:** Social (Supporting — JTBD 6)
**Causas ←:** [Factor externo: payroll systems diseñados para bank transfers]
**Efectos →:** UDE-6-S-01
**Evidencia:** [inferido — formal employment requiere bank account en la mayoría de países para payroll; es barrera documentada de empleo formal]

---

## Meta-UDE

### UDE-META-01
**Enunciado:** Sin acceso a servicios financieros formales, 1,287M de adultos quedan excluidos de la protección, las oportunidades y la dignidad que el sistema financiero formal provee a sus clientes — y las alternativas informales (cash, ROSCA, prestamistas) tienen costos结构和 riesgos nadie cuantifica ni ofrece como solución sistémica.
**Tipo:** Meta
**Causas ←:** UDE-1-E-01, UDE-2-E-01, UDE-3-E-01, UDE-4-E-01, UDE-5-E-01, UDE-6-E-01, UDE-7-E-01
**Efectos →:** UDE-1-S-01, UDE-2-S-01, UDE-3-S-01, UDE-4-S-01, UDE-5-S-01, UDE-6-S-01, UDE-7-S-01
**Evidencia:** 26% de unbanked dice que la barrera principal es documentación insuficiente, no falta de fondos — el problema es diseño del sistema, no del individuo. [1]

## Matriz de referencia rápida

| ID | Tipo | Causas ← | Efectos → |
|----|------|-----------|--------|
| UDE-1-F-01 | F | [ext] | 1-E-01, 6-F-01 |
| UDE-1-F-02 | F | [ext] | 1-F-01 |
| UDE-2-F-01 | F | [ext] | 2-E-01 |
| UDE-3-F-01 | F | [ext] | 3-E-01, 5-F-01 |
| UDE-3-F-02 | F | [ext] | 3-F-01 |
| UDE-4-F-01 | F | [ext] | 4-E-01 |
| UDE-4-F-02 | F | 4-F-01 | 4-E-01 |
| UDE-5-F-01 | F | 3-F-01 | 5-E-01 |
| UDE-6-F-01 | F | [ext] | 6-E-01, 6-S-01 |
| UDE-6-F-02 | F | [ext] | 6-S-01 |
| UDE-7-F-01 | F | [ext] | 7-E-01 |
| UDE-7-F-02 | F | 2-F-01 | 7-E-01 |
| UDE-1-E-01 | E | 1-F-01 | META-E |
| UDE-2-E-01 | E | 2-F-01 | META-E |
| UDE-3-E-01 | E | 3-F-01 | META-E |
| UDE-4-E-01 | E | 4-F-01, 4-F-02 | META-E |
| UDE-5-E-01 | E | 5-F-01 | META-E |
| UDE-6-E-01 | E | 6-F-01 | META-E |
| UDE-7-E-01 | E | 7-F-01, 7-F-02 | META-E |
| UDE-7-E-02 | E | 7-F-01 | 7-E-01 |
| UDE-1-S-01 | S | 6-F-01, 1-F-01 | META-S |
| UDE-2-S-01 | S | 2-F-01 | META-S |
| UDE-3-S-01 | S | 3-F-01, 5-F-01 | META-S |
| UDE-4-S-01 | S | 4-F-01 | META-S |
| UDE-5-S-01 | S | 5-F-01 | META-S |
| UDE-6-S-01 | S | 6-F-01, 6-F-02 | META-S |
| UDE-7-S-01 | S | 7-F-01 | META-S |
| UDE-META-01 | M | 1-E→7-E | 1-S→7-S |
