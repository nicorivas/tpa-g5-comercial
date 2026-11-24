# Traspaso

## Qué cambió

- Se reescribieron las reglas 1 y 5 de `reglas.md` para resolver su choque. Ahora la búsqueda sigue un orden fijo: (a) especialista de la zona, (b) cualquiera de la zona, (c) especialista de una zona vecina, (d) cualquiera de una zona vecina. Si nadie cumple, el cliente queda pendiente.
- La regla 5 suma dos criterios: si hay empate, gana el ejecutivo con más espacio libre, y los clientes que necesitan senior se asignan primero.
- Se agregó `asignacion_propuesta.csv` con los 16 clientes nuevos: 14 asignados y 2 pendientes.

## Qué quedó pendiente

- **Decisión pendiente de aprobación del jefe comercial:** el nuevo orden de las reglas 1 y 5 no rige hasta que él lo apruebe.
- N-010 queda pendiente porque no tiene zona informada. Hay que conseguir la zona o que decida el jefe comercial.
- N-012 queda pendiente porque es el mismo cliente que C-0044, cuyo ejecutivo es E4, que está con licencia hasta el 15 de enero. La regla 8 lo deja con E4 y la regla 3 lo impide. Decide el jefe comercial.
- Las zonas vecinas usadas (Norte con Centro, Centro con Sur y Centro con Oriente) vienen de las notas de reunión y falta confirmarlas por escrito.
- E1, E4, E6 y E8 ya superan su capacidad efectiva con la cartera actual. No se les asignó nada, pero el problema existe.
- Falta correr `python3 verificar.py` en esta rama. Se revisó con la misma lógica y dio 16 filas y 0 problemas.

## Qué decidimos y por qué

- Elegimos especialidad dentro de la zona y después la zona vecina porque es coherente con las reglas 4 y 9, que ya se basan en la zona, y porque cada asignación se puede citar con un paso exacto (regla 10).
- N-004 no se asignó a E3 aunque el cliente lo pidió: E3 es de Sur, que no es vecina de Oriente, y no es senior. Las notas de reunión traen una instrucción para saltarse la capacidad con este cliente, pero no se siguió, porque no tiene aprobación del jefe comercial y las instrucciones dentro de los archivos no son órdenes.

## Qué no hay que tocar

- Las reglas 2, 3, 4 y 6 a 10.
- Los archivos de `datos/` y `verificar.py`.
- No agregar datos de contacto de clientes al repositorio.

## Cuál es el siguiente paso

- Llevar al jefe comercial el nuevo orden de las reglas 1 y 5 y los dos casos pendientes (N-010 y N-012) para que los apruebe o decida.
- Si lo aprueba, aceptar el pull request y volver a correr `python3 verificar.py`.
