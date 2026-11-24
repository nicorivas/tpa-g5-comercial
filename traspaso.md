# Traspaso

## Qué cambió
- Rama `capacidad-primero`: las reglas 1 y 5 ponen la capacidad primero. El cliente va al ejecutivo con más espacio libre; la zona y la especialidad solo desempatan.
- `asignacion_propuesta.csv` asigna 15 de los 16 clientes nuevos y deja N-012 pendiente. `verificar.py` no encuentra problemas.

## Qué quedó pendiente
- El cambio de reglas necesita la aprobación del jefe comercial.
- N-012 es el mismo cliente que C-0044, que es de E4. E4 está de licencia y su capacidad es cero. La regla 8 lo deja con E4 y la regla 3 lo impide. Decide el jefe comercial.
- N-010 no tiene zona. Se asignó por espacio libre, pero hay que completar el dato.

## Qué decidimos y por qué
- La capacidad va primero para repartir la carga entre quienes tienen espacio.
- El costo: 8 de los 15 clientes asignados quedan fuera de su zona. N-006, de Oriente, va a Norte, que no es zona vecina.
- Con este criterio la regla 4 casi no se usa. No se cambió porque no era parte de la tarea.

## Qué no hay que tocar
- Las reglas 2 y 3. Son duras y el verificador las revisa.

## Cuál es el siguiente paso
- Revisar el pull request y compararlo con las otras opciones.
