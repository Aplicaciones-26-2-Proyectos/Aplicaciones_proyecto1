# Proyecto 1 — Aplicaciones en Ciencia de Datos

Proyecto académico de análisis exploratorio de **Características y composición del hogar**. La base de trabajo tiene 235.350 registros y 78 variables. Coincide en nombre, tamaño y variables con el [archivo de la Encuesta Nacional de Calidad de Vida 2025 del DANE](https://microdatos.dane.gov.co/index.php/catalog/905/data-dictionary/F9?file_name=Caracteristicas+y+composicion+del+hogar). No se conservó el enlace exacto desde el que se descargó esta copia.

El notebook ya carga la base y diagnostica identificadores, duplicados, faltantes, tipos y valores únicos. La limpieza, el análisis y las conclusiones siguen pendientes.

## Archivos de trabajo

- `datos/raw/caracteristicas_composicion_hogar.csv`: copia sin modificaciones del archivo proporcionado para este proyecto. Usa `;` como separador y coma decimal.
- `notebooks/01_limpieza_preparacion.ipynb`: notebook del proyecto. Carga la base correcta y presenta un diagnóstico inicial de calidad, sin eliminar ni imputar datos.
- `datos/procesados/`: espacio reservado para una versión preparada; todavía no se ha generado para esta base.
- `requirements.txt`: dependencias de Python.

Los archivos de AnAge usados por error se retiraron de la copia de trabajo; siguen recuperables en el historial de Git. El significado de las variables codificadas se consulta en el diccionario oficial antes de decidir transformaciones. No se han eliminado filas ni rellenado valores faltantes.

## Ejecución

Instala las dependencias con `pip install -r requirements.txt` y ejecuta el notebook desde la raíz del repositorio o desde `notebooks/`.
