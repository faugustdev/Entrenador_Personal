# Documentación Entrenador Personal
El Entrenador Personal, es un sitema de recomendación de rutinas y alimentación.

1. ## **Procesamiento de Datos**
He considerado necesario la utilización del mapeo de índice único, principalmente para mantener la integridad de los datos, al evitar la inserción de registros duplicados, asegurando que cada entrada sea distinta.  Luego loa aplicamos al DataFrame asignándole un conjunto específico de valores de índice único al mismo. 
Finalmente realizamos un 'merge'(combinación) de los DataFrames utilizando la función 'pd.merge'de la biblioteca Pandas en Python. El merge se realiza utilizando los índices de los DataFrames.
   
2. ## **Modelo**
El modelo de recomendación utilizado, se basa en técnicas de procesamiento del lenguaje natural, se centra en técnicas avanzadas de las mismas y utiliza la medida de similitud del coseno  
para ofrecer recomendaciones personalizadas a partir de un formulario de preguntas.

## **Componentes Principales del Modelo**
1. ### **Representación del Texto:**
   La representación del texto, se logra mediante el uso de la técnica TF-IDF (Term Frequency-Inverse Document Frequency). Esto permite transformar las descripciones de rutas y alimentos en vectores numéricos, 
capturando la importancia relativa de los términos en función de su frecuencia en los documentos y su rareza en el conjunto de datos.
2. ### **Similitud del Coseno:**
   La similitud del coseno se emplea para medir la proximidad semántica entre las descripciones codificadas y las preguntas del formulario. Este enfoque permite calcular la similitud entre vectores, proporcionando una medida eficaz de cuán relacionados están dos textos.

**Ajuste Práctico del Modelo:**
Dado el tamaño modesto del conjunto de datos, se ha adoptado un enfoque pragmático. Se ha decidido no realizar ajustes exhaustivos de parámetros, como max_features y ngram_range, para evitar posibles problemas de sobreajuste. Dada la limitada cantidad de datos, se prioriza mantener el modelo relativamente simple y evitar la complejidad que podría no ser justificada por la cantidad de información disponible.

**Umbral de Similitud:**
El modelo incluye un umbral de similitud que actúa como criterio para filtrar las recomendaciones. Este umbral se ajusta para equilibrar la cantidad de recomendaciones con la relevancia deseada.

** Evaluación Continua:**
El modelo se somete a una evaluación continua para monitorear su rendimiento y realizar ajustes según sea necesario. Este enfoque adaptativo es fundamental para mejorar la efectividad del modelo a medida que se recopilan más datos o se obtiene una comprensión más profunda del comportamiento del usuario.
