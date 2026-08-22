# El relevamiento completo

`relevamiento_completo.csv` es el conjunto de datos de la clase 3: cuarenta filas y ocho columnas.
Es el mismo relevamiento de la clase 2, ahora entero. **Las doce primeras filas son, idénticas, las
doce de `clase-2-captura-y-variables/datos/relevamiento.csv`.**

El notebook lo fabrica en el momento, así que funciona sin conexión. Esta copia existe para que el
notebook pueda leerla una vez desde su dirección web, igual que en la clase 2.

La clase 2 diagnosticó y no tocó nada. La clase 3 limpia, y para eso el archivo trae estos defectos:

| Dónde | Qué tiene | Sección |
|---|---|---|
| Fila 40 | Repite entera la fila 39: duplicado exacto | 3.1 |
| `id` 41 | Aparece dos veces con contenido distinto: conflicto | 3.3 |
| `localidad` | Siete formas de escribir tres localidades | 5.1 |
| `fecha_visita` | Treinta y seis fechas ISO y cuatro en `dd/mm/aaaa` | 5.2 |
| `ingreso`, hogar 3 | Vacío de verdad | 4.1 |
| `ingreso`, hogar 9 | `999999`, un centinela | 4.1 |
| `ingreso`, hogar 38 | `0`, que es un ingreso real y no una ausencia | 4.1 |
| `ingreso`, hogar 39 | `620000`, el extremo en el que los dos métodos coinciden | 5.4 |
| `ingreso`, hogar 7 | `310000`, el extremo en el que **no** coinciden | 5.4 |
| `personas`, hogar 39 | `12`, extremo en una variable discreta | 5.4 |
| `cobertura_salud` y `satisfaccion` | El texto `NULL` en las mismas diez filas | 4.4 |
| `servicios` | Cuatro servicios en una celda, con dos separadores distintos | 6.4 |

## Los números que importan

El arco de la limpieza es **40 filas, 39 sin el duplicado exacto, 37 hogares** una vez descartadas
las dos filas en conflicto del `id` 41, que son dos filas y un solo hogar.

En `ingreso`, sin contar el centinela, el IQR marca tres valores y el z-score marca dos. El que
queda en discusión es el `310000` del hogar 7, que el alumno ya conoce de la clase 2. En `personas`
los dos métodos coinciden en el `12`. Esa diferencia es la lección de la sección 5.4.

Las dos filas que usan coma en lugar de punto y coma van entre comillas dobles, como pide el
[RFC 4180](https://datatracker.ietf.org/doc/html/rfc4180). Por eso `str.get_dummies(sep=";")`
devuelve seis columnas donde debería devolver cuatro, sin dar ningún error.
