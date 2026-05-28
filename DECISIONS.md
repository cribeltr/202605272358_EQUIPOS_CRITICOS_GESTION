# Decisiones de diseño y arquitectura

Registro tipo ADR liviano. Formato:

```
## [N] [Título]
**Fecha**: YYYY-MM-DD
**Estado**: aceptada | revertida | superada por [N]
**Contexto**: ...
**Decisión**: ...
**Razón**: ...
**Alternativas consideradas**: ...
**Consecuencias**: ...
```

---

## [1] HTML único autocontenido en `dist/`, sin build step en V1

**Fecha**: 2026-05-28
**Estado**: aceptada
**Contexto**: CLAUDE.md exige V1 como HTML autocontenido sin dependencias npm ni build step. Se evaluó si separar fuente en `/src/*.css` + `/src/*.js` + script de concatenación, o mantener todo inline en el HTML.
**Decisión**: todo inline en `dist/gestion_mp_hhha.html`. `data/data.json` se conserva como referencia legible del esquema y se mantiene en sincronía manual con el bloque embebido.
**Razón**: en esta etapa el archivo cabe en <50 KB. Un build step añade fricción operativa para Cristian (que abre el HTML directo en navegador) sin beneficio observable. Si el archivo cruza ~150 KB de código fuente o se vuelve incómodo de editar, se introduce `build.py`.
**Alternativas consideradas**: separar src + build.py desde el inicio (rechazada por complejidad prematura).
**Consecuencias**: deuda técnica baja por la duplicación de datos JSON; aceptable mientras los datos sean de prueba.

