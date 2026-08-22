# El relevamiento de la clase 2

`relevamiento.csv` es el conjunto de datos que usa toda la clase 2: doce hogares y ocho columnas.
Es un dato **inventado**, con defectos puestos a propósito, y está descrito en la sección 1.3 del
apunte.

El notebook lo fabrica en el momento, así que funciona sin conexión. Esta copia existe por una sola
razón: el notebook la lee una vez desde su dirección web, para mostrar que `pd.read_csv` acepta una
URL igual que acepta una ruta de archivo. Es la única celda del notebook que necesita internet, y
ninguna otra depende de ella.

Los defectos plantados son estos:

| Dónde | Qué tiene |
|---|---|
| `id` | Huecos en la numeración: falta el 6 y el 12 |
| `localidad` | Cinco valores distintos para tres localidades |
| `localidad`, hogar 9 | Un espacio al final, invisible en pantalla |
| `fecha_visita` | Texto, no fecha |
| `ingreso`, hogar 3 | Vacío de verdad |
| `ingreso`, hogar 9 | `999999`, un valor centinela |
| `cobertura_salud` y `satisfaccion` | El texto `NULL` en las mismas cuatro filas |
| `servicios` | Cuatro servicios en seis combinaciones, en una sola celda |
