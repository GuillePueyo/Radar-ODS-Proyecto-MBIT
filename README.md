# Radar-ODS-Proyecto-MBIT
Se trata de un predictor de Objetivos de Desarrollo Sostenible Mediante la App eAgora, los usuarios introducen comentarios para proponer iniciativas, actividades, publicidad etc. Nuestor modelo evalúa este comentario y le aplica uno o varios ODS's. A través de es ejercicio, podemos llevar una medición de ODSs a nivel nacional.

En los archivos de este proyecto existe la siguiente información;
 - Notebooks de Python
 - Memoria del proyecto
 - Dataset de entrenamiento
 - Esquema de trabajo y rendimiento de modelos
 - Modelos entrenados con extensión .pkl
 
### `1. Notebooks`
 - `TFM con dataset eAgora.ipynb` ; este notebook contiene el ejercicio de prueba usando un dataset de mala calidad y solo en catalán. Lo hemos añadido como parte del proyecto y para tener en cuenta el tiempo invertido
 - `TFM_FINAL.ipynb` ; **este notebook contiene todo el proyecto**. Lo exponemos por apartados;
    1. *Entrenamiento y rendimiento de modelo*; todos los pasos están detallados para entender el proceso.
    2. *Conexión y predicción de comentarios de la App eAgora*; conectamos directamente con la tabla SQL que almacena los comentarios de los usuarios.
    3. *Aplicación DASH*; generación de una interfaz gráfica para predecir ODS's de manera dinámica.
    4. *Función auxiliar*; al final del notebook existe una función que puede servir en el futuro para seguir haciendo predicciones. Simplemente es una función que toma de ejemplo el formato de otra tabla (también en este repositorio llamado contenidos y etiquetas_proba.xlsx)
 
### `2. Memoria`
 - Se puede hacer uso de la memoria para un mayor entendimiento del proyecto. En la memoria se detalla con más exactitud el problema a resolver además de una propuesta de escalabilidad.

### `3. Dataset`
 - Se debe informar al lector que el dataset de entrenamiento ha sido creado a mano de manera artificial. Por ello, el predictor está limitado y en varias ocasiones no predecirá nada. Esto es normal ya que la probablidad sería tan baja que el modelo directmanete no lo muestra. Decir también que está en castellano y catalán.

### `4. Modelos`
 - Se pueden usar directamente los modelos sin necesidad de ejecutar el notebook entero mediante `joblib.load()`

### `5. Dashboard - Power BI`
 - Se trata de un dashboard a modo de ejemplo usando los datos de nuestro dataset con la inclusión del nombre de algunos ayuntamientos para poder tener análisis por yuntamiento a modo de prueba.
 - La información está almacenada en S3 y es de dominio público por lo que todo el mundo puede "jugar" con el Dashboard.
