# Evaluación Parcial N°2 - Técnicas de Regularización en Deep Learning

Notebook de evaluación MLP con Fashion-MNIST.

Este repositorio contiene el notebook desarrollado para la Evaluación Parcial N°2 de la asignatura Fundamentos de Deep Learning.

El objetivo del trabajo es continuar el modelo MLP desarrollado en la Evaluación Parcial N°1 y aplicar técnicas de regularización para analizar su impacto en el rendimiento, la estabilidad del entrenamiento y la capacidad de generalización del modelo.

## Dataset utilizado

Se utiliza el dataset Fashion-MNIST, compuesto por imágenes de prendas de vestir en escala de grises. Cada imagen tiene un tamaño de 28x28 píxeles y es transformada a un vector de 784 características para ser utilizada en el modelo MLP.

## Técnicas implementadas

En el notebook se desarrollan y comparan las siguientes técnicas:

- Modelo baseline MLP de la EP1
- L2 Regularization con λ = 0.001 y λ = 0.01
- Dropout con tasas 0.2 y 0.5
- Batch Normalization
- Early Stopping con patience = 5 y patience = 20
- Modelo final regularizado combinando Batch Normalization, Dropout 0.2 y Early Stopping
- Bonus: Data Augmentation con ruido gaussiano

## Bonus: Data Augmentation

Como experimento adicional, se aplicó Data Augmentation agregando ruido gaussiano leve a los datos de entrenamiento.

La idea fue generar pequeñas variaciones en las imágenes para entregar mayor variedad al modelo y evaluar si esta técnica ayudaba a mejorar la generalización.

El experimento bonus obtuvo el mejor resultado global:

- Accuracy: 0.8876
- F1-score: 0.8866

## Métricas utilizadas

Para comparar los modelos se utilizaron las siguientes métricas:

- Accuracy
- Precision
- Recall
- F1-score

Además, se incluyen gráficos de accuracy y pérdida para analizar el comportamiento del entrenamiento y la validación.

## Instrucciones de ejecución

1. Abrir el notebook en Google Colab.

2. Descomprimir el archivo ZIP llamado `Fashion`. Dentro de esa carpeta deben estar los siguientes 4 archivos:

   - train-images-idx3-ubyte.gz
   - train-labels-idx1-ubyte.gz
   - t10k-images-idx3-ubyte.gz
   - t10k-labels-idx1-ubyte.gz

3. Subir esos 4 archivos directamente a la carpeta /content de Google Colab.  
   Esto es importante porque el notebook carga los datos desde esa ubicación.

4. Ejecutar las celdas del notebook desde el inicio hasta el final.

5. Revisar los resultados obtenidos: métricas, gráficos de entrenamiento/validación, tabla comparativa y conclusiones finales.

## Resultados generales

El modelo baseline de la EP1 fue utilizado como punto de comparación para evaluar el impacto de las técnicas de regularización.

El modelo final regularizado combinó Batch Normalization, Dropout 0.2 y Early Stopping con patience=5, obteniendo un rendimiento equilibrado dentro de las técnicas obligatorias:

- Accuracy: 0.8765
- F1-score: 0.8763

Además, el experimento bonus de Data Augmentation obtuvo el mejor resultado global:

- Accuracy: 0.8876
- F1-score: 0.8866

## Conclusión general

Los resultados muestran que no todas las técnicas de regularización mejoran automáticamente el rendimiento del modelo. Algunas configuraciones, como L2 con λ = 0.01 y Dropout 0.5, redujeron el desempeño, mientras que Dropout 0.2 y Early Stopping mostraron un comportamiento más equilibrado.

El modelo final regularizado fue el mejor dentro de las técnicas obligatorias, mientras que Data Augmentation obtuvo el mejor resultado global como experimento bonus. Esto indica que agregar pequeñas variaciones a los datos de entrenamiento puede ayudar a mejorar la generalización del modelo.

Como mejora futura, se podría probar una arquitectura CNN, ya que al trabajar con imágenes podría capturar mejor patrones como bordes, formas y texturas.
