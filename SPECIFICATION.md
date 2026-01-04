# Especificación técnica

1. Origen (epoch)

- El día D0 es la fecha origen definida por el usuario (p. ej. fecha de nacimiento).
- Contadores 0-based.

2. Unidad atómica

- 1 día = 24 horas (usar UTC para conversión canónica).

3. Jerarquía decimal

- d: día dentro del bloque (0–9)
- B: bloque (10 días)
- H: hectablock (100 días, opcional)
- K: kiloblock (1000 días, opcional)

4. Cálculos canónicos

D = días totales desde el origen

K = floor(D / 1000)
H = floor((D % 1000) / 100)
B = floor((D % 100) / 10)
d = D % 10

Formato humano principal: `B,d` (ej.: `1325,3`)
Formato posicional completo: `K,H,B,d` (ej.: `13,2,5,3`)

5. Reglas

- Todas las conversiones deben usar UTC medianoche para evitar ambigüedades de huso.
- La implementación de referencia debe documentar la elección de origen y permitir usar fechas locales para visualización.
