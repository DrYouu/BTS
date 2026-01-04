# Sistema de Tiempo en Bloques (BTS)

Presentación

BTS (Block Time System) es un sistema personal y determinista de indexación del tiempo basado en bloques decimales de 10 días. Está diseñado para organización personal, seguimiento de hábitos y archivo de eventos a largo plazo. Esta versión en castellano es la principal; las fuentes en inglés se han movido a `legacy/english/`.

Objetivos

- Proveer una forma regular y decimal de agrupar días.
- Eliminar dependencias de años, meses irregulares y semanas arbitrarias.
- Facilitar la planificación y el seguimiento mediante notación posicional.

Ventajas frente a calendarios tradicionales

- Regularidad completa: bloques de 10 días uniformes.
- Notación decimal compatible con aritmética mental.
- Fácil indexación a largo plazo sin ajustes por años bisiestos.
- Conversiones posibles hacia/desde calendarios civiles cuando se necesita interoperabilidad.

Idea central

- Unidad atómica: el día (24 h).
- Bloque (B): 10 días.
- Notación principal: `B,d` (por ejemplo, `B1325,3`).
- Origen (epoch) personal: el día 0 se define por el usuario (p. ej. fecha de nacimiento).

Guía rápida (Quickstart)

1. Define tu origen (fecha base).
2. Para convertir una fecha civil a BTS:
   - Convierte la fecha civil a UTC medianoche.
   - Calcula días transcurridos D desde el origen.
   - Calcula B = floor(D/10) y d = D % 10.
3. Para convertir de BTS a civil:
   - D = 10·B + d
   - Suma D días al origen y muestra la fecha civil.

Documentación incluida

- `PHILOSOPHY.md` — Fundamentos y razones del diseño.
- `SPECIFICATION.md` — Especificación técnica y formatos.
- `CONVERSION.md` — Métodos de conversión y notas de interoperabilidad.
- `EXAMPLES.md` — Ejemplos de uso y casos prácticos.
- `FAQ.md` — Preguntas frecuentes.
- `CALENDAR_2026.md` — Calendario de muestra para 2026.
- `CALENDAR_2026.ics` — Archivo iCalendar con los inicios de bloque para 2026.

Contacto

Repositorio: https://github.com/DrYouu/BTS

Contribuciones y mejoras: las instrucciones básicas se encuentran en `legacy/english/` para referencia en inglés. Esta rama principal y los archivos en castellano constituyen el núcleo visible.
