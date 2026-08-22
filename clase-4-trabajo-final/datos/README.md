# Los datasets provistos para el trabajo final

Tres conjuntos de datos **reales**, descargados de portales de datos abiertos en agosto de 2026 y
guardados acá sin ninguna modificación. Existen para que el trabajo final no dependa de que el
portal del organismo esté en línea, y para quien prefiere no buscar un dataset propio.

Están ordenados de más fácil a más difícil. Los tres cumplen los requisitos de la consigna y los
tres tienen problemas reales de sobra: nadie los ensució a propósito.

| Archivo | Origen | Filas x Cols | Se lee con |
|---|---|---|---|
| `participacion_ciudadana.csv` | Secretaría de Comunicación, CABA | 2 182 x 15 | por defecto |
| `calidad_aire_2017.csv` | Agencia de Protección Ambiental, CABA | 8 652 x 11 | `sep=";"` |
| `bafici_films_2015.csv` | Ministerio de Cultura, CABA | 2 131 x 15 | `sep=";"`, `encoding="latin-1"` |

Qué trae cada uno, verificado sobre estas copias:

- **Participación Ciudadana. Propuestas.** 920 filas completamente vacías, que son también los
  919 duplicados: es un problema, no dos. Fechas como texto en `dd/mm/aa`. Nombres de columna con
  espacios, mayúsculas y acentos.
- **Calidad de aire 2017.** Decimal con coma, que deja diez de las once columnas como texto. Tres
  marcadores de faltante distintos (`" "`, `s/d`, `S/D`) conviviendo en las mismas columnas, más un
  valor censurado (`<0,05`) que no es un faltante. Un BOM al principio del archivo. Formato ancho:
  una columna por estación y contaminante.
- **BAFICI. Films 2015.** Encoding roto en origen y sin arreglo limpio: la columna `aã±o` se
  llama así en el archivo. Unos 39 registros de prueba (`test en prd`) mezclados con los films.
  Duración con la unidad pegada al número (`"76 min"`).

Los tres son datasets publicados bajo licencia abierta por el Gobierno de la Ciudad de Buenos
Aires en [Buenos Aires Data](https://data.buenosaires.gob.ar/dataset/). La ficha de cada dataset,
con su licencia y su frecuencia de actualización, vive en el portal: buscarla es parte del trabajo.
