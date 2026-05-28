# Changelog

Bitácora cronológica de ajustes al proyecto. Formato:

```
## [YYYY-MM-DD HH:MM] · [Título corto]
**Pedido por Cristian**: ...
**Archivos tocados**: ...
**Cambios**: ...
**Riesgos identificados y mitigados**: ...
**Verificaciones realizadas**: ...
```

---

## [2026-05-28 04:30] · Estructura base + Equipos funcional + hoja de vida modal + import/export

**Pedido por Cristian**: armar el programa en HTML partiendo por estructura base + datos de prueba.
**Archivos tocados**: `data/data.json`, `dist/gestion_mp_hhha.html`, `docs/Flujo_Trabajo_HHHA.docx`, `STATUS.md`, `DECISIONS.md`, `TESTS.md`, `BACKLOG.md`.
**Cambios**:
- Estructura de carpetas: `src/`, `data/`, `dist/`, `docs/`.
- `data/data.json` v1.0 con 13 equipos de prueba (7 familias, 8 servicios), 8 eventos cronológicos, 3 pendientes y 13 filas de programación 2026.
- HTML autocontenido en `dist/gestion_mp_hhha.html` (~36 KB): header con título + import/export + botón Grabar (stub deshabilitado), navegación de 5 pestañas, paleta papel hueso / tinta / verde médico, tipografía Fraunces + IBM Plex Sans + JetBrains Mono.
- Pestaña Equipos: tabla densa con 9 columnas, header sticky, filtros (familia / servicio / estado / búsqueda libre con debounce 150ms), contador de resultados, click en fila abre hoja de vida.
- Modal hoja de vida: metadata grid (8 campos), pendientes vigentes, bitácora cronológica de eventos (más reciente arriba). Cierra con × / Escape / click fuera.
- Las otras 4 pestañas quedan como placeholders ("en construcción") para no romper la navegación.
- Import / Export JSON funcionales con feedback toast.
**Riesgos identificados y mitigados**:
- Duplicación de datos entre `data.json` y HTML embebido → registrado como deuda técnica baja.
- Botón Grabar visible pero deshabilitado → declarado en plan, próximo sub-ajuste.
**Verificaciones realizadas**:
- JSON embebido se parsea correctamente (`json.loads` ok).
- 13 equipos, 8 eventos, 3 pendientes detectados.
- Tamaño HTML 36 KB (límite V1: 2 MB).

---

## [2026-05-28 04:05] · [META] Bootstrap de archivos de memoria

**Pedido por Cristian**: cargar el proyecto a partir de `CLAUDE.md` recién entregado.
**Archivos tocados**: `CLAUDE.md`, `STATUS.md`, `CHANGELOG.md`, `BACKLOG.md`, `DECISIONS.md`, `TESTS.md`.
**Cambios**:
- Se copió `CLAUDE.md` al repo (estaba solo en el upload).
- Se crearon los 5 archivos de memoria vacíos con sus encabezados, según sección 0 del CLAUDE.md.
**Riesgos identificados y mitigados**: ninguno (no hay código aún).
**Verificaciones realizadas**: estructura de archivos verificada; rama `claude/intelligent-meitner-M1Tys` activa.
