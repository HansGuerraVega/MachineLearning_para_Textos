# Descripción del proyecto
Film Junky Union, una nueva comunidad vanguardista para los aficionados de las películas clásicas, está desarrollando un sistema para filtrar y categorizar reseñas de películas. Tu objetivo es entrenar un modelo para detectar las críticas negativas de forma automática. Para lograrlo, utilizarás un conjunto de datos de reseñas de películas de IMDB con etiquetado para construir un modelo que clasifique las reseñas como positivas y negativas. Este deberá alcanzar un valor F1 de al menos 0.85.

## Pasos
Carga los datos.
Preprocesa los datos, si es necesario.
Realiza un análisis exploratorio de datos y haz tu conclusión sobre el desequilibrio de clases.
Realiza el preprocesamiento de datos para el modelado.
Entrena al menos tres modelos diferentes para el conjunto de datos de entrenamiento.
Prueba los modelos para el conjunto de datos de prueba.
Escribe algunas reseñas y clasifícalas con todos los modelos.
Busca las diferencias entre los resultados de las pruebas de los modelos en los dos puntos anteriores. Intenta explicarlas.
Mostrar:
- un poco de análisis exploratorio de datos con algunos gráficos;
- evaluate_model(): una rutina para evaluar un modelo de clasificación que se ajusta a la interfaz de predicción de scikit-learn;
- BERT_text_to_embeddings(): una ruta para convertir lista de textos en insertados con BERT.
El trabajo principal es construir y evaluar modelos.

Se probarán modelos de clasificación basados en regresión logística y potenciación del gradiente, pero puedes probar otros métodos. Puedes jugar con la estructura de la plantilla del proyecto siempre y cuando sigas sus instrucciones.

No tienes que usar BERT para el proyecto porque requiere mucha potencia computacional y será muy lento en la CPU para el conjunto de datos completo. Debido a esto, BERT generalmente debe ejecutarse en GPU para tener un rendimiento adecuado. Sin embargo, puedes intentar incluir BERT en el proyecto para una parte del conjunto de datos. Si deseas hacer esto, te sugerimos hacerlo de manera local y solo tomar un par de cientos de objetos por cada parte del conjunto de datos (entrenamiento/prueba) para evitar esperar demasiado tiempo. Asegúrate de indicar que estás usando BERT en la primera celda (el encabezado de tu proyecto).

## Descripción de los datos
Los datos se almacenan en el archivo imdb_reviews.tsv.

Los datos fueron proporcionados por Andrew L. Maas, Raymond E. Daly, Peter T. Pham, Dan Huang, Andrew Y. Ng, y Christopher Potts. (2011). Learning Word Vectors for Sentiment Analysis. La Reunión Anual 49 de la Asociación de Lingüística Computacional (ACL 2011).

Aquí se describen los campos seleccionados:

review: el texto de la reseña
pos: el objetivo, '0' para negativo y '1' para positivo
ds_part: 'entrenamiento'/'prueba' para la parte de entrenamiento/prueba del conjunto de datos, respectivamente
Hay otros campos en el conjunto de datos, puedes explorarlos si lo deseas.
