# CRT — Unbanked Population

## Análisis de conectividad

Conteo de veces que cada UDE-ID aparece en campos "Efectos →" de otros UDEs (fan-in):

| UDE | Fan-in | Tipo |
|-----|--------|------|
| UDE-META-01 | 14 (suma de todos los UDEs Emocionales y Sociales) | Meta |
| UDE-3-F-01 | 2 (UDE-5-F-01 ← 3-F-01, UDE-3-S-01 ← 3-F-01) | F |
| UDE-4-F-01 | 2 (UDE-4-F-02 ← 4-F-01, UDE-4-E-01 ← 4-F-01) | F |
| UDE-5-F-01 | 2 (UDE-5-E-01 ← 5-F-01, UDE-5-S-01 ← 5-F-01) | F |
| UDE-6-F-01 | 3 (UDE-6-E-01 ← 6-F-01, UDE-6-S-01 ← 6-F-01, UDE-1-S-01 ← 6-F-01) | F |
| UDE-7-F-01 | 3 (UDE-7-E-01 ← 7-F-01, UDE-7-S-01 ← 7-F-01, UDE-7-E-02 ← 7-F-01) | F |
| UDE-2-F-01 | 2 (UDE-7-F-02 ← 2-F-01, UDE-2-E-01 ← 2-F-01) | F |

**Nodo de mayor fan-in funcional:** UDE-6-F-01 y UDE-7-F-01 (3 incoming cada uno). Esto los convierte en palancas candidatas.

---

## Árbol ASCII

```
╔══════════════════════════════════════════════════════════════════════════════╗
║                           CAUSAS RAÍZ EXTERNAS                               ║
╚══════════════════════════════════════════════════════════════════════════════╝

  [ext-1]                          [ext-2]                          [ext-3]
 Diseño de sistemas de pago       Falta de productos de           Scoring models requieren
 diseñados para clientes           ahorro diseñados para           historial crediticio formal
 bancarios. No existe             no-bancarios. No hay             — bootstrapping imposible.
 on-ramp para quienes               producto formal de              Sin collateral físico
 no tienen cuenta.                 ahorro accesible en            disponible para no-asset-
                                   áreas rurales ni urbanas.        holders. Microfinance
                                                                       requiere group liability.

       │                               │                                │
       ▼                               ▼                                ▼
╔══════════════════════╗    ╔══════════════════════╗         ╔══════════════════════╗
║ UDE-1-F-01           ║    ║ UDE-2-F-01            ║         ║ UDE-3-F-01            ║
║ 1,287M no pueden     ║    ║ 43% de ahorros en     ║         ║ 74% crédito en África ║
║ recibir/enviar pagos║    ║ casa o con             ║         ║ Subsahariana es        ║
║ electrónicos sin    ║    ║ family/friends         ║         ║ informal              ║
║ cuenta bancaria     ║    ║ (riesgo robo/pérdida) ║         ║                       ║
╚══════════════════════╝    ╚══════════════════════╝         ╚══════════════════════╝
       │                               │                                │
       │                               │                                │
       ▼                               ▼                                ▼
╔══════════════════════╗    ╔══════════════════════╗         ╔══════════════════════╗
║ UDE-6-F-01           ║    ║ UDE-7-F-02            ║         ║ UDE-5-F-01            ║
║ 45% de unbanked en    ║    ║ ROSCA requiere grupo  ║         ║ Hogares de bajo ingreso║
║ India tiene móvil     ║    ║ social pre-existente  ║         ║ pagan 5x más por      ║
║ pero no acceso a      ║    ║ (y es vulnerable a    ║         ║ productos financieros ║
║ servicios digitales  ║    ║ default no recoverable)║        ║ comparables           ║
╚══════════════════════╝    ╚══════════════════════╝         ╚══════════════════════╝
       │                               │                                │
       │                               │                                │
       ▼                               ▼                                ▼
╔══════════════════════╗    ╔══════════════════════╗         ╔══════════════════════╗
║ UDE-1-F-02           ║    ║ UDE-2-E-01           ║         ║ UDE-5-E-01            ║
║ Mobile money requiere║    ║ Anxiety por seguridad║        ║ Fear de espiral de    ║
║ teléfono + cobertura ║    ║ del efectivo en casa  ║         ║ deuda que no se puede ║
║ (no universal)       ║    ║                        ║         ║ salir                 ║
╚══════════════════════╝    ╚══════════════════════╝         ╚══════════════════════╝
       │
       ▼
╔══════════════════════╗
║ UDE-6-F-02           ║
║ Employers requieren   ║
║ bank account para    ║
║ payroll (no hay      ║
║ alternativa formal) ║
╚══════════════════════╝
       │
       ▼
╔═══════════════════════════════════════╗
║            CAPA EMOCIONAL             ║
║    (punto de convergencia de          ║
║     los bloqueos funcionales)        ║
╠═══════════════════════════════════════╣
║                                       ║
║  UDE-1-E-01  Frustración de exclus-  ║
║              ión de transacciones    ║
║              digitales básicas       ║
║                     │                ║
║                     ▼                ║
║  UDE-2-E-01  Anxiety por seguridad   ║
║              del ahorro en casa     ║
║                     │                ║
║                     ▼                ║
║  UDE-3-E-01  Vergüenza de pedir      ║
║              prestado a family/friends║
║                     │                ║
║                     ▼                ║
║  UDE-4-E-01  Anxiety por si la       ║
║              remesa llegará a tiempo║
║                     │                ║
║                     ▼                ║
║  UDE-5-E-01  Fear de caer en        ║
║              espiral de deuda        ║
║                     │                ║
║                     ▼                ║
║  UDE-6-E-01  Sentimiento de          ║
║              obsolescencia frente a ║
║              la economía digital     ║
║                     │                ║
║                     ▼                ║
║  UDE-7-E-01  Fear de shock sin       ║
║              red de protección      ║
║                     │                ║
║                     ▼                ║
║  UDE-7-E-02  Stress financiero      ║
║              se convierte en        ║
║              conflicto doméstico    ║
║                     │                ║
║                     ▼                ║
║          ╔════════════════╗          ║
║          ║  UDE-META-01  ║          ║
║          ║  META-UDE —   ║          ║
║          ║  Mayor fan-in  ║          ║
║          ║  (14 refs)     ║          ║
║          ╚════════════════╝          ║
║                 │                    ║
║                 ▼                    ║
║          CAPA SOCIAL                ║
║   (efectos downstream del META)      ║
╠═══════════════════════════════════════╣
║                                       ║
║  UDE-1-S-01  Exclusión de plataformas║
║              de trabajo freelance   ║
║                     │                ║
║  UDE-2-S-01  Efectivo vulnerable a  ║
║              uso no autorizado en   ║
║              el hogar               ║
║                     │                ║
║  UDE-3-S-01  Default informal daña  ║
║              capital social (stigma) ║
║                     │                ║
║  UDE-4-S-01  Alto costo de remesas  ║
║              daña relationships      ║
║              familiares             ║
║                     │                ║
║  UDE-5-S-01  Stigma de debt cierra  ║
║              oportunidades en      ║
║              comunidad pequeña      ║
║                     │                ║
║  UDE-6-S-01  Digital divide amplifi-║
║              ca inequality existente║
║                     │                ║
║  UDE-7-S-01  Shock médico produce  ║
║              ausentismo escolar,    ║
║              trabajo infantil       ║
╚═══════════════════════════════════════╝
```

---

## Loops de refuerzo

### Loop 1: Exclusión financiera auto-sostenida

```
UDE-6-E-01 (sentimiento obsolescencia)
    │
    ▼
[creencia: "el sistema me exclude, no vale la pena intentar"]
    │
    ▼
UDE-6-S-01 (digital divide amplifica inequality)
    │
    ▼
[menos oportunidades de income → más necesidad de crédito informal]
    │
    ▼
UDE-5-F-01 (tasas 5x más altas por no-bancar)
    │
    ▼
UDE-5-E-01 (fear de espiral de deuda)
    │
    ▼
[evita pedir prestado → no puede aprovechar oportunidades → más frustración]
    │
    ▼
UDE-1-E-01 (frustración exclusión transacciones digitales)
    │
    ▼
[de vuelta a UDE-6-E-01]
```

**Punto de quiebre:** Romper en UDE-6-F-01 — si existe alternativa de payment que no requiere bank account, se corta la cadena antes de que llegue a la frustración emocional.

### Loop 2: Ahorro inseguro → deuda cara → más riesgo

```
UDE-2-F-01 (43% guarda ahorros en casa sin protección)
    │
    ▼
UDE-2-E-01 (anxiety por seguridad del efectivo)
    │
    ▼
[no hay producto de ahorro diseñado para este segmento → única opción es cash]
    │
    ▼
UDE-7-F-02 (ROSCA requiere grupo social — pero si el grupo se rompe, se pierde todo)
    │
    ▼
[si shock grande > capacidad del ROSCA → necesita crédito]
    │
    ▼
UDE-3-F-01 (74% crédito informal en SSA)
    │
    ▼
UDE-5-F-01 (tasas 5x más altas para no-bancarios)
    │
    ▼
[no puede pagar → default → daña capital social]
    │
    ▼
[ menos ayuda disponible en próxima emergencia → más dependiente de crédito informal]
    │
    ▼
[de vuelta a UDE-2-F-01]
```

**Punto de quiebre:** UDE-3-F-01. Si existe forma de acceder a crédito sin pasar por prestamistas informales, se rompe la conexión default → círculo vicioso.

---

## Palanca candidata

**Identificación:** La palanca es el UDE o factor que:
1. Afecta el mayor número de UDEs downstream
2. Está dentro de al menos 1 loop
3. Es accionable por actor privado

| Criterio | UDE-6-F-01 | UDE-7-F-01 | UDE-3-F-01 |
|---------|-----------|-----------|-----------|
| Fan-in (refs entrantes) | 3 | 3 | 2 |
| Afecta loops | Loop 1 | Loop 2 | Loop 2 |
| Accionable por actor privado | ✅ | ✅ | ✅ |
| Rompe loops | Sí (rompe Loop 1) | Indirecto | Sí (rompe Loop 2) |

**Decisión: UDE-6-F-01 es la palanca primaria.**

Rationale:
- Es el nodo de mayor fan-in (3 refs causales)
- Es el punto de quiebre del Loop 1
- Si se habilita un mecanismo de payment digital sin bank account, se ataca la causa raíz de múltiples UDEs downstream
- Es accionable por actor privado (no requiere regulación bancaria)

**Palanca secundaria: UDE-3-F-01.** Si se rompe el crédito informal como única opción (mediante alternativa P2P o grupal), se corta el Loop 2.

---

## Fase 04 — Iceberg (appendida en el mismo archivo)

### Estructura Sistémica (EST)

**EST-1: Sistemas de pago diseñados para banking, no para personas.**
El diseño de toda la infraestructura de payments (POS, online gateways, mobile wallets vinculados a bank accounts, payroll systems) asume que el usuario tiene cuenta bancaria. Esta asunción está embedded en cada layer — regulatorio, tecnológico, comercial — y hace que construir alternativas sin cuenta sea posible pero costoso y complejo.

**EST-2: Scoring crediticio requiere historial formal, pero el historial solo se construye usando el sistema formal.**
 chicken-and-egg del credit building. Para tener score necesitas credit history; para tener credit history necesitas access a crédito. Este loop impide que los no-bancarios construyan el collateral que necesitarían para acceder a productos formales.

**EST-3: Savings informales no tienen protección institucional.**
El efectivo guardado en casa y los ROSCA son mecanismos de savings que existen porque no hay alternativa formal adecuada — pero no tienen protección contra robo, pérdida, o default del organizer. Cuando fallan, el daño es catastrophic para el participante individual.

**EST-4: Income informal no es reconocible por sistemas formales.**
Freelancers, gig workers, trabajadores Informales tienen income real pero volatile. Los sistemas formales (applications de crédito, payroll, tax) no pueden verify income informal — leading to exclusion even when income is sufficient.

### Modelos Mentales (MM)

**MM-1: "Si no tienes cuenta bancaria, no confío en tu capacidad de pago."**
En la lógica del sistema financiero formal, bank account = verification of identity + financial behavior. Sin eso, counterparties en transactions (empleadores, lenders, platforms) no tienen manera de trust sin expensive verification processes.

**MM-2: "El efectivo físico es el único dinero real."**
En comunidades no-bancarias, el cash es tangible, visible, controlable. El dinero en una cuenta bancaria es abstracto, propiedad del banco, accesible solo a través de él. Este MM dificulta la adopción de cualquier alternativa que no sea cash.

**MM-3: "Pedir prestado a la familia es gratis y sin riesgo."**
La noción de que loans familiares no tienen costo ni consequence es falsa — tienen costo relacional, riesgo de shame, y potential de daño al capital social. Pero este MM es difícil de romper porque está deeply embedded en culture de comunidades.

**MM-4: "Los que no tienen cuenta bancaria es porque no trabajan lo suficiente."**
Blame atribuido al individuo. Este MM justifica la inacción de policy makers y la indiferencia del sector privado. Perpetúa el cycle al no address las barreras estructurales que son system-designed.

---

**Nota:** Este documento es appendible. La sección Iceberg puede crecer si los artefactos de fase 04 revelan nuevas ESTs o MMs.
