# Traspaso

## Qué cambió
- Rama `regla-1-zona-primero` (autor B).
- La regla 1 dice ahora que la zona pasa antes que la especialidad. La especialidad solo desempata.
- Se creó `asignacion_propuesta.csv` con los 16 clientes nuevos. `verificar.py` no encuentra problemas.

## Qué quedó pendiente
- N-010 no tiene zona, así que la regla 1 no se puede aplicar.
- N-012 es el mismo cliente que C-0044. Por la regla 8 va a E4, pero E4 está de licencia.
- E1, E4, E6 y E8 ya tienen más clientes que su capacidad efectiva.

## Qué decidimos y por qué
- Si la especialidad no desempata, se elige al ejecutivo con más espacio libre. A igual espacio, al que no es senior. Así se guarda el cupo senior para los clientes de la regla 2.
- Los clientes se asignan en el orden del archivo.
- Para la regla 4 se usaron las zonas vecinas de `notas-reunion.md`. Falta que se confirmen por escrito.

## Qué no hay que tocar
- `datos/`, que es la fuente de la propuesta.
- `verificar.py`.

## Cuál es el siguiente paso
- Revisar el pull request con `REVIEW.md`.
- Unir esta rama con la del autor A. Van a chocar en `reglas.md`, en `asignacion_propuesta.csv` y en este archivo.
- Llevar al jefe comercial los pendientes y los dos criterios de desempate. El cambio de regla necesita su aprobación.
