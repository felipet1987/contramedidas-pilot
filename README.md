# Contramedidas Mining — Public Pilot: Unbanked Population

> Pipeline completado públicamente. Cada commit = una fase completada. Sin edición retrospectiva.

**Dominio:** Población unbanked — adultos sin acceso a cuenta bancaria tradicional por requisitos de income verification, credit history, o documentación.

**Claim:** Este pilot valida la metodología Contramedidas Mining en un dominio agnóstico (no Chile-specific). Los resultados son específicos del dominio unbanked. La metodología es adaptable a otros dominios; cada dominio requiere su propio pilot.

## Progreso

| Fase | Estado | Commit |
|------|--------|--------|
| 01 Research | ✅ Completada | `dca8ca3` |
| 02 UDEs | ✅ Completada | `554d8fe` |
| 03 CRT | ✅ Completada | `c2cf4e8` |
| 04 Iceberg | ✅ Completada (appendida a CRT) | `c2cf4e8` |
| 05 TOC | ✅ Completada | `2e3d6be` |
| 06 Countermeasures | ✅ Completada | `e43244b` |
| 07 HDD | ✅ Completada | `204c117` |
| 08 Report | ✅ Completada | `860187b` |

## Artefactos generados

```
cm-analysis/
├── research/unbanked-jtbd-2026-05-11.md     — 7 JTBD clusters + meta-JTBD
├── udes/unbanked-udes-2026-05-11.md        — 27 UDEs (F/E/S/Meta)
├── crt/unbanked-crt-2026-05-11.md           — 2 loops, 4 ESTs, 4 MMs
├── toc/unbanked-toc-2026-05-11.md           — evaporating cloud, 3 QWs TOC
├── countermeasures/unbanked-qws-2026-05-11.md — 6 QWs, roadmap 3 fases
├── hdd/unbanked-hypotheses-2026-05-11.md    — 4 HYP cards, MVE, metrics
└── reports/
    ├── report-unbanked-2026-05-11.md        — reporte markdown
    └── report-unbanked-2026-05-11.html      — McKinsey-style HTML
```

## Resumen de hallazgos

- **6 Quick Wins** identificados, 2 en Fase 1 (lanzable <60 días)
- **Palanca primaria:** Mobile money como payment on-ramp sin bank account
- **2 loops de refuerzo** identificados con puntos de quiebre claros
- **4 hypotheses** con MVE, metrics, umbrales de validación/invalidación

## Lecciones aprendidas

1. **Research Mode B (existing data)** funciona bien para dominios con datos públicos de calidad (World Bank Findex). No requiere deep-research skill.
2. **UDEs inferidos** son necesarios cuando la evidencia cuantitativa no tiene cifra directa — usar "[inferido]" + nota explicativa.
3. **CRT con 27 UDEs** genera árbol con profundidad suficiente para 14 refs al META-UDE (≥10 requirement pasado).
4. **Loop identification** requiere leer el árbol de abajo hacia arriba — fácil pasar por alto loops si no se busca explícitamente.
5. **Fase 04 iceberg** puede appenderse al CRT sin archivo separado si el CRT doc es suficientemente largo.

## Contexto

El repo `contramedidas-mining` contiene la metodología. Este repo es el pilot público que la valida.

Ver `contramedidas-mining/` para la metodología completa.