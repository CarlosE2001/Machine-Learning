### **Práctica 6: Redes Neuronales <br>Análisis de Grandes Volúmenes de Datos CI-<br>Carlos Espinoza B92786 <br>I-2022**

# **How to Choose an Activation Function for Deep Learning**

## **Funciones de Activación**

Una función de activación dentro de una red neuronal es el método por el cual la suma de las entradas de una neurona generan una salida de uno o varios nodos dentro de una red neuronal. Si el rango de salida de una neurona es limitado, este se llama `squashing function`.

La elección de la función de activación tiene un gran impacto en la capacidad y el rendimiento de la red. Diferentes funciones de activación pueden ser utilizados en diferentes capas del modelo.

Tipicamente las redes neuronales tienen 3 capas (input, hidden y output) ellas tienen, generalemente, funciones de activación distintas

## **Activación para las Capas Ocultas**

Las capas ocultas son las que se encuentran en el medio, reciben de la capa de entrada o de otra capa oculta, entregan su salida a la capa de salida o a otra capa oculta. 

Funciones de activación para la capa oculta:
- **Rectified Linear Activation (ReLU):** Es la más común de las funciones de activación. Es simple de implementar y efectiva para sobrellevar limitaciones

- **Logistic (Sigmoid):** Es la misma función usada en `logistic regression classification algorithm`

- **Hyperbolic Tangent (Tanh):** Toma los valores entre -1 y 1. Entre más grande sea el input, más cercana a 1 será la salida

## **¿Cómo escoger la función de activación para la capa oculta?**

- **Perceptron Multi Capa:** ReLU
- **Convolutional Neural Network:** ReLU
- **Recurrent Neural Network:** Sigmoid/Tanh

## **Activación para capas de salida**

Esta es la capa que devuelve directamente un valor

Funciones de activación para la capa de salida:

- **Linear Output:** Es generalmente llamada `identidad`, esto porque esta función no cambia el valor de la suma de las señales de entrada, sino que devuelve el valor directo

- **Sigmoid Output:** Es la función descrita anteriormente

- **Softmax Output:** Devuelve un vector de números que sumados pueden dar la probabilidad de una entrada sea miembro de una clase

## **¿Cómo escoger la función de activación para la capa de salida?**

- **Regression**: One node, linear activation.
- **Binary Classification:** One node, sigmoid activation.
- **Multiclass Classification:** One node per class, softmax activation.
- **Multilabel Classification:** One node per class, sigmoid activation.