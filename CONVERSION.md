# Conversión entre calendarios

De Gregorian a BTS

1. Normalizar la fecha civil a UTC medianoche.
2. Calcular D = número de días enteros desde la fecha origen (día 0).
3. Calcular B = floor(D/10) y d = D % 10.
4. Mostrar `B,d` o `K,H,B,d` según prefieras.

De BTS a Gregorian

1. Calcular D = 10·B + d.
2. Sumar D días a la fecha origen.
3. Mostrar la fecha civil resultante (en UTC o en hora local, según la interfaz).

Notas de interoperabilidad

- Los años bisiestos y variaciones civiles se manejan en la capa de conversión; no afectan la estructura BTS.
- Para intercambio de datos con otros sistemas, incluir la fecha origen explicita (ISO 8601) junto con cualquier valor BTS.
