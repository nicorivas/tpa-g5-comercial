# Traspaso

## Qué cambió

- En la rama `regla5-especialidad-antes-que-zona`, la regla 5 ahora dice que la especialidad pasa antes que la zona.
- Se creó `asignacion_propuesta.csv` con los 16 clientes nuevos: 14 asignados y 2 pendientes.
- `python3 verificar.py` da 0 problemas.

## Qué quedó pendiente

- N-010 no tiene zona. Hay tres ejecutivos de oficina con espacio y sin zona no se puede elegir entre ellos.
- N-012 es el mismo cliente que C-0044, que está con E4. E4 está de licencia y tiene capacidad cero. Lo decide el jefe comercial.
- El jefe comercial tiene que aprobar el cambio de la regla 5 antes de aceptarlo.
- Falta confirmar por escrito las zonas vecinas. N-004 depende de que Centro sea vecina de Oriente.

## Qué decidimos y por qué

- Las reglas 2 y 3 se cumplen siempre, antes que la especialidad.
- Si hay varios especialistas con espacio, se prefiere el de la zona del cliente y después el de una zona vecina.
- Si no hay especialista con espacio, se asigna al ejecutivo de la zona con más espacio libre.
- Varios clientes quedaron con ejecutivos de otra zona. Por ejemplo, N-008 de Norte y N-014 de Oriente quedaron con E7, de Sur. Es el efecto esperado de la nueva regla.

## Qué no hay que tocar

- Los archivos de `datos/`.
- La regla 1. La cambia el autor B en su propia rama.

## Cuál es el siguiente paso

- Revisar el pull request con `REVIEW.md` y llevar al jefe comercial el cambio de regla y los dos pendientes.
