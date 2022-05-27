### **Práctica 6: Redes Neuronales <br>Análisis de Grandes Volúmenes de Datos CI-<br>Carlos Espinoza B92786 <br>I-2022**

# **Crash Course On Multi-Layer Perceptron Neural Networks**

## Conceptos básicos 

- **Perceptrones Multi-Capa:** Los perceptrones son simplemente un modelo de una sola neurona que se desarrollaron antes de las redes neuronales más grandes. <br>
El poder predictivo de las redes neuronales viene de la estructura multi capa de las redes. 

- **Neuronas:** Un bloque importante que conforma las redes neuronales son las neuronas artificiales. Son simples unidades computacionales que tienen una entrada con peso que producen una señal de salida mediante una función de activación.

	- **Peso de neuronas:** Similares a los coeficientes utilizados en las ecuaciones de regresión. Son inicializadas generalemente con valores aleatorios entre `0-0.3`

	- **Activación:** Los valores entrantes son sumados y pasados por una función de activación. Esta función lo único que hace es mapear un valor de entrada a un valor de salida

- **Redes de Neuronas:** Las neuronas son puestas en una red de neuronas. Unas fila de neuronas es llamada `capa` 

- **Entrada o Capas Visibles**: La capa del fondo es la que recibe la señal directa que viene del dataset. Se llama capa visible porque es la parte más expuesta de la red. No son neuronas, simplemente pasan la información a la primera capa

- **Capas ocultas:** La última capa oculta es llamada la capa de salida. Es responsable de entregar el valor o conjunto de valores. La decisión de tener una función de activación el la capa de salida va a depender del tipo de problema

	- **Regresión:** Una neurona de salida sin función de activación
	- **Clasificación Binaria:** Una neurona con función de activación que de una predicción de las clases
	- **Clasificación Multi Clase:** Múltiples neuronas en la capa de salida, una para cada clase. Tiene una función de activación

## Entrenamiento de Redes

### **Preparación de los datos**

Los datos deben ser números, por ejemplo, números reales. Si se tienen valores categóricos estos deben ser transformados a valores numéricos representativos. Se debe agregar una columna por cada clase categórica.

Se debe aplicar la normalización, es decir se deben ajustar los valores a un rango entre `0 y 1`

### **Stochastic Gradient Descent**

Es el algoritmo clásico y preferido para el entrenamiento de las redes neuronales. En esta parte es que la red se ve expuesta a la primera fila de datos. La red va a procesar los valores entrantes y los va a mandar hacia arriba activando las neuronas en su paso. El tipo de paso es el que más adelante va a permitir la predicción de clases.

El resultado dado por la última capa es comparado con el valor esperado para poder obtener el error calculado. Este error es enviado a cada capa para que se ajusten los pesos. `Backpropagation Algorithm`.

### **Actualización de los Pesos**

Los pesos de las neuronas pueden ser actualizados por el error calculado en cada entrenamiento y es llamado aprendizaje en línea. Puede resultar en cambios rápidos pero caóticos de la red. Otra técnica es almacenar los errores para que sean procesados hasta el final del entrenamiento, esto se llama `batch learning`

La cantidad de peso que es ajustada es controlada por medio de la configuración de un parámetro llamado `learning rate`

### **Predicción**

Una vez que se entrena a una red neuronal esta puede ser utilizada para realizar predicciones. Se pueden hacer predicciones en datos de prueba o validación.