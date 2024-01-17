# Documentación Entrenador Personal
El Entrenador Personal, es un sitema de recomendación de rutinas y alimentación.

## **Modelo**
El modelo de recomendación utilizado, se basa en técnicas de procesamiento del lenguaje natural, se centra en técnicas avanzadas de las mismas y utiliza la medida de similitud del coseno  
para ofrecer recomendaciones personalizadas a partir de un formulario de preguntas.

## **Componentes Principales del Modelo**
1. ### **Representación del Texto:**
   La representación del texto, se logra mediante el uso de la técnica TF-IDF (Term Frequency-Inverse Document Frequency). Esto permite transformar las descripciones de rutas y alimentos en vectores numéricos, 
capturando la importancia relativa de los términos en función de su frecuencia en los documentos y su rareza en el conjunto de datos.
