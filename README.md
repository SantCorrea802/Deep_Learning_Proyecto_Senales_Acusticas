# Detección y clasificación de eventos acústicos de aves presentes en Colombia mediante aprendizaje profundo

**Ingeniería de Sistemas**

**Santiago Correa Marulanda**

**Email**: <santiago.correa7@udea.edu.co>

## Proyecto de Deep Learning

### Preparación del corpus

Los notebooks:

- `01_construccion_metadata_canonica.ipynb`
- `02_construccion_manifests_modelado.ipynb`

se conservan en este repositorio como **evidencia y documentación del proceso utilizado para preparar los datos y construir los manifests del proyecto**. Estos notebooks **no están diseñados para ser reproducidos directamente por terceros**, ya que fueron ejecutados durante la etapa inicial de preparación del corpus y dependen de una estructura específica de archivos y rutas en Google Drive.

El notebook `01_construccion_metadata_canonica.ipynb` documenta la construcción de los primeros manifests a partir de los metadatos fuente y de los audios originales.

El notebook `02_construccion_manifests_modelado.ipynb` documenta la transformación de dichos manifests en los archivos utilizados posteriormente para el modelado, incluyendo los manifests correspondientes al detector y al clasificador.

**No es necesario ejecutar estos dos notebooks para continuar con las etapas posteriores del proyecto**. Los resultados generados durante esta etapa de preparación, junto con los audios remuestreados a 32 kHz y los metadatos necesarios para continuar el proyecto, se encuentran publicados en el siguiente dataset de Kaggle: [Kaggle Dataset](https://www.kaggle.com/datasets/santiagocorrea802/dataset-proyecto).

La estructura completa utilizada durante la preparación inicial también se conserva en una carpeta pública de Google Drive: [Google Drive del proyecto](https://drive.google.com/drive/folders/1UrRMs98CDUBre2bHOVamXNBl13agqLbq?usp=sharing), esta carpeta contiene los audios originales, audios remuestreados, metadatos fuente y demás archivos empleados durante la preparación. Debido a su tamaño, superior a los 100 GB antes del procesamiento, no se recomienda reconstruir esta etapa salvo que se quiera auditar detalladamente el procedimiento realizado.


### Análisis Exploratorio

- `03_analisis_exploratorio.ipynb`  
Este notebook realiza el análisis exploratorio del corpus y justifica decisiones de modelado, incluyendo:
- duración candidata de ventanas
- rango frecuencial
- coocurrencia de eventos
- solapamiento entre bounding boxes
- disponibilidad de regiones sin anotaciones
- partición train/validation/test por `recording_uid`

Este notebook usa los manifests procesados y está orientado a justificar las decisiones previas al entrenamiento de los modelos.
