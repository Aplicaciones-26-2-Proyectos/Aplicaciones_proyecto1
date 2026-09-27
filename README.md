# Proyecto 1 — Aplicaciones en Ciencia de Datos

Proyecto académico de análisis exploratorio de **Características y composición del hogar**. La base de trabajo tiene 235.350 registros y 78 variables. Coincide en nombre, tamaño y variables con el [archivo de la Encuesta Nacional de Calidad de Vida 2025 del DANE](https://microdatos.dane.gov.co/index.php/catalog/905/data-dictionary/F9?file_name=Caracteristicas+y+composicion+del+hogar). No se conservó el enlace exacto desde el que se descargó esta copia.

El notebook carga la base, diagnostica su calidad, genera una copia preparada conservadora y verifica que los demás datos no cambiaron. Mantiene todas las filas y retira únicamente dos columnas completamente vacías. El análisis y las conclusiones siguen pendientes.

## Archivos de trabajo

- `datos/raw/caracteristicas_composicion_hogar.csv`: copia sin modificaciones del archivo proporcionado para este proyecto. Usa `;` como separador y coma decimal.
- `notebooks/01_limpieza_preparacion.ipynb`: notebook del proyecto. Documenta el diagnóstico y prepara una copia sin eliminar registros ni imputar respuestas.
- `datos/procesados/caracteristicas_composicion_hogar_preparado.csv`: copia con 235.350 filas y 76 columnas; se retiraron `P3510S1` y `P3510S2` porque están totalmente vacías, pero se conservaron sus subcolumnas con datos.
- `requirements.txt`: dependencias de Python.

Los archivos de AnAge usados por error se retiraron de la copia de trabajo; siguen recuperables en el historial de Git. El significado de las variables codificadas se consulta en el diccionario oficial antes de decidir transformaciones. No se han eliminado filas ni rellenado valores faltantes. Las columnas con más del 80 % de vacíos, pero con alguna respuesta, quedan señaladas en el notebook para revisión según el cuestionario; no se borran automáticamente.

## Ejecución

Instala las dependencias con `pip install -r requirements.txt` y ejecuta el notebook desde la raíz del repositorio o desde `notebooks/`.

## Para continuar el proyecto

El equipo puede usar `datos/procesados/caracteristicas_composicion_hogar_preparado.csv` como punto de partida para el análisis. La unidad de observación es la persona, no el hogar. Antes de calcular indicadores, debe confirmar en el diccionario qué significa cada código y cómo utilizar `FEX_C`, el factor de expansión. Los vacíos parciales y los códigos especiales no se transformaron porque su tratamiento depende de las preguntas analíticas elegidas.
