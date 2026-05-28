# Estado del proyecto

**Última actualización**: 2026-05-28
**Avance V1**: ~22% (≈1.5 de 7 features útiles)

## Features completadas
- [x] Estructura base del programa (header, nav 5 pestañas, layout, paleta, tipografía)
- [x] Pestaña Equipos: tabla densa, filtros (familia / servicio / estado), búsqueda libre, contador de resultados
- [x] Hoja de vida (modal) — versión mínima: metadata + pendientes vigentes + bitácora cronológica
- [x] Import / Export JSON

## Features en curso
- (ninguna)

## Features pendientes (V1)
- [ ] Dashboard (KPIs, alertas >30 días, pendientes abiertos, MP del mes, últimos eventos)
- [ ] Programación MP (Gantt anual filtrable con códigos P/R)
- [ ] Eventos (bitácora consolidada con filtros)
- [ ] Pendientes (gestión con estado y compromisos)
- [ ] Grabación de uso (telemetría local — botón visible pero deshabilitado)

## Deuda técnica conocida
- Datos embebidos duplicados entre `dist/gestion_mp_hhha.html` y `data/data.json` — se sincronizan a mano por ahora (severidad baja). Si crece, agregamos `build.py`.
- Botón "● Grabar" presente pero deshabilitado (severidad baja, planificado).

## Bugs abiertos
- (ninguno)

## Métricas
- Ajustes implementados: 1 (estructura + Equipos + modal + import/export)
- Regresiones acumuladas: 0
- Decisiones registradas: 1
- Ítems en backlog: 4 (V2)
- Cobertura checklist manual: 0/12 (a verificar)
