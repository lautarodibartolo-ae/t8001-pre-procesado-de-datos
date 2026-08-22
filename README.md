# T8001 — Pre-procesado de datos

Taller de nivelación de 12 horas de cursada repartidas en cuatro clases. El material son cuatro
notebooks de Google Colab, uno por clase. El botón los abre en Colab, sin instalar nada.

| Clase | Modalidad | |
|---|---|---|
| 1 — Tipos de datos, archivos y formatos | Asincrónica | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lautarodibartolo-ae/t8001-pre-procesado-de-datos/blob/main/clase-1-tipos-y-formatos/01_tipos_y_formatos.ipynb) |
| 2 — Captura y análisis de la información de entrada | Sincrónica | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lautarodibartolo-ae/t8001-pre-procesado-de-datos/blob/main/clase-2-captura-y-variables/02_captura_y_variables.ipynb) |
| 3 — Limpieza, codificación, normalización y gráficos | Sincrónica | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lautarodibartolo-ae/t8001-pre-procesado-de-datos/blob/main/clase-3-limpieza-y-graficos/03_limpieza_y_graficos.ipynb) |
| 4 — Trabajo final | Asincrónica | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lautarodibartolo-ae/t8001-pre-procesado-de-datos/blob/main/clase-4-trabajo-final/04_trabajo_final.ipynb) |

## De qué se trata

Pre-procesado de datos es un taller de nivelación de la Especialización en Inteligencia de Datos
para la Gestión Estratégica, orientado a la preparación de los datos que antecede a cualquier
análisis. Entre el 60% y el 80% del tiempo de un proyecto de datos se va en esa preparación, y el
taller trabaja sobre esa parte: de dónde sale un dato, qué problemas trae, cómo se diagnostican y
qué se decide en cada uno.

El eje es el criterio sobre los datos y no la programación. Casi ninguna operación de limpieza
tiene una única respuesta correcta, así que se evalúa la justificación de cada decisión y la
reproducibilidad del proceso, no la elegancia del código. El material está pensado también para
estudiantes sin experiencia previa en programación: la clase 1 arranca con una ruta de capítulos
sueltos de un curso de Python en YouTube, y cada bloque se lee, después se ejecuta una demostración
ya escrita, y recién al final se completa un ejercicio corto, que no necesariamente hay que
resolver en Python.

Las clases 1 y 4 son asincrónicas y cada estudiante las recorre a su ritmo. Las clases 2 y 3 son
encuentros virtuales sincrónicos teórico-prácticos, y el docente los recorre en vivo ejecutando
cada celda. Los notebooks de las sincrónicas están escritos para las dos cosas: sirven de guion en
clase y se pueden releer después.

Por eso también el stack es mínimo: `pandas` y `matplotlib`, más `Pillow` en un solo bloque y la
biblioteca estándar. Nada de `numpy` explícito, `seaborn`, `scikit-learn` ni herramientas de
perfilado automático. Donde una librería resolvía el problema en una línea y escondía el concepto,
se escribió el concepto.

Las tres primeras clases usan un mismo dataset real y sucio: `SAFI`, una encuesta a hogares
agrícolas del proyecto Studying African Farmer-led Irrigation. En el trabajo final cada estudiante
trabaja sobre un dataset real: uno de los tres provistos en el repositorio, o uno que elija de un
portal de datos abiertos.

## Contenidos

- **Clase 1** — Tipos de datos y de archivos. Conversión entre formatos. Compresión con pérdida y
  sin pérdida. Contenido y metadatos. Codificación de caracteres. Importación y exportación.
- **Clase 2** — Recuperación de datos. Mecanismos de captura, error y sesgo. Tipos de variables y
  escalas de medición. Diccionario de variables. Análisis de la información de entrada.
- **Clase 3** — Limpieza y transformación: faltantes, duplicados, texto, fechas, valores extremos y
  celdas con varios valores. Codificación y normalización. Representaciones gráficas.
- **Clase 4** — Todo lo anterior, sobre un dataset real que elige cada estudiante. La consigna y
  la guía de pasos están en el documento de la clase; el notebook es un ejemplo terminado del
  pipeline entero. Se recomienda entregarlo como notebook y se acepta cualquier herramienta.

Cada clase declara en su encabezado qué se aprende. La única entrega del taller es el trabajo
final, que es opcional y recomendada; las actividades de las clases 1 a 3 quedan como práctica y
no se corrigen.

## Licencia

Este material se publica bajo [CC BY 4.0](LICENSE): se puede usar, copiar y adaptar libremente,
con atribución. El dataset SAFI tiene la misma licencia y es del proyecto
[Studying African Farmer-led Irrigation](https://datacarpentry.github.io/socialsci-workshop/data/).
