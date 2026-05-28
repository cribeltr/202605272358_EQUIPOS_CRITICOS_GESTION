# Checklist de verificación manual

Estos son los tests que se ejecutan mentalmente (o en navegador) en cada autoauditoría.

---

## Estructura base
- [ ] Abrir `dist/gestion_mp_hhha.html` en Chrome/Edge muestra header + 5 pestañas + vista Equipos por defecto.
- [ ] Las fuentes Fraunces / IBM Plex Sans / JetBrains Mono cargan correctamente.
- [ ] Click en cada pestaña cambia la vista (las 4 placeholders muestran "en construcción").

## Equipos
- [ ] Tabla muestra 13 equipos de prueba con sus 9 columnas.
- [ ] Header de tabla queda sticky al hacer scroll vertical.
- [ ] Filtro **Familia** acota la lista a la familia elegida.
- [ ] Filtro **Servicio** acota la lista al servicio elegido.
- [ ] Filtro **Estado** acota la lista al estado elegido.
- [ ] Búsqueda libre encuentra por N° inventario, equipo, marca, modelo, serie, servicio, ubicación.
- [ ] Búsqueda es case-insensitive.
- [ ] Combinación de filtros funciona (familia + servicio + búsqueda simultáneos).
- [ ] Botón "Limpiar filtros" resetea todo.
- [ ] Contador "X de Y equipos" se actualiza con cada filtro.
- [ ] Badges de estado (Operativo verde / No operativo terracota / Servicio técnico ámbar / Baja gris) se renderizan con sus colores.

## Hoja de vida (modal)
- [ ] Click en una fila abre el modal del equipo correcto.
- [ ] Modal muestra metadata, pendientes vigentes y bitácora cronológica.
- [ ] Bitácora ordena los eventos del más reciente al más antiguo.
- [ ] Equipos sin eventos muestran "Sin eventos registrados."
- [ ] Equipos sin pendientes muestran "Sin pendientes abiertos."
- [ ] Cerrar con × funciona.
- [ ] Cerrar con tecla Escape funciona.
- [ ] Cerrar haciendo click fuera del modal funciona.

## Import / Export
- [ ] "Exportar JSON" descarga archivo con nombre `gestion_mp_hhha_[fecha-hora].json`.
- [ ] Archivo exportado tiene la misma estructura que el inicial (version, meta, catalogos, equipos, eventos, pendientes, programacion).
- [ ] "Importar JSON" con archivo válido reemplaza el estado en memoria.
- [ ] Tras importar, los filtros se resetean y la tabla muestra los nuevos equipos.
- [ ] Importar archivo inválido (sin campo `equipos`) muestra alerta clara y no rompe el estado actual.

## Dashboard
- (pendiente de implementación)

## Programación MP
- (pendiente de implementación)

## Eventos
- (pendiente de implementación)

## Pendientes
- (pendiente de implementación)

## Grabación de uso
- (pendiente de implementación)
