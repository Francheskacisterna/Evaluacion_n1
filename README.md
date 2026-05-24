# Evaluacion_n1
Notebook de evaluación MLP con Fashion-MNIST

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
- Modelo final regularizado combinando técnicas

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

   - `train-images-idx3-ubyte.gz`
   - `train-labels-idx1-ubyte.gz`
   - `t10k-images-idx3-ubyte.gz`
   - `t10k-labels-idx1-ubyte.gz`

3. Subir esos 4 archivos directamente a la carpeta `/content` de Google Colab.  
   Esto es importante porque el notebook carga los datos desde esa ubicación.

4. Ejecutar las celdas del notebook desde el inicio hasta el final.

5. Revisar los resultados obtenidos: métricas, gráficos de entrenamiento/validación, tabla comparativa y conclusiones finales.

## Conclusión general

Los resultados muestran que no todas las técnicas de regularización mejoran automáticamente el rendimiento del modelo. En este caso, la combinación de Batch Normalization, Dropout 0.2 y Early Stopping permitió obtener un modelo final más estable y equilibrado, manteniendo un buen desempeño en datos de prueba.
