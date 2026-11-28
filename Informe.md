# Datos a tener en cuenta para el informe
A continuación dejaré anotado algunas consideraciones para armar el informe:

# Arquitectura inicial del autoencoder convolucional

Se tomó como punto de partida la arquitectura convolucional presentada en el material de la cátedra. El modelo está compuesto por un codificador (encoder) y un decodificador (decoder), cada uno con dos capas convolucionales.

El codificador utiliza convoluciones con kernels de 3 × 3, stride de 2 y padding de 1, seguidas de funciones de activación ReLU. Estas capas transforman las imágenes de entrada de 1 × 28 × 28 en una representación latente de 32 × 7 × 7, reduciendo progresivamente la resolución espacial.

El decodificador utiliza dos convoluciones transpuestas para recuperar las dimensiones originales. Finalmente, se aplica una función Sigmoid para obtener reconstrucciones en el intervalo [0, 1], consistente con el preprocesamiento de las imágenes.

Esta arquitectura se utilizó como modelo de referencia (*baseline*) para iniciar los experimentos y evaluar posteriormente posibles modificaciones mediante el conjunto de validación.


# Función pérdida
El optimizador elegido con dicho learnig rate se corresponde con el baseline propuesto.
