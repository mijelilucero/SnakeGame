# 🎮 **Análisis del Juego Snake**

Básicamente, el juego **Snake** inicializa la serpiente en el centro del área de juego y obtiene una posición aleatoria para la comida. La serpiente inicia únicamente con un segmento, el cual es la cabeza, pero a medida que va coincidiendo con la posición de la comida, va agregando nuevos segmentos a su cola.

En este repositorio incluí:  
- **La versión original dada en clase**
- **La versión generada con IA**
- **La versión que yo modifiqué para que funcionara correctamente**

---

## 🚀 **La Versión Original**

La versión original funciona mediante un **arreglo**, lo que hace que su funcionamiento sea más simple, pues a un arreglo se le pueden quitar elementos al final y agregar elementos al principio. Pero lo solicitado era modificar este código para implementar la clase **Cola** realizada en clase.

---

## 🤖 **La Versión Generada con IA**

En primera instancia, utilicé **ChatGPT**, **GitHub Copilot** y **Claude** para realizar las modificaciones correspondientes para que la serpiente fuera una cola e implementara sus respectivos métodos.

Sin embargo, los códigos generados presentaban el error de que se utilizaban de manera incorrecta los métodos de `enqueue` y `dequeue`. De manera que, inicialmente, la cabeza se encontraba en el índice 0. Luego, si la serpiente no comía, se realizaba un `dequeue` quitando la cabeza del principio, y luego se hacía un `enqueue` con la nueva cabeza. Esto provocaba que la serpiente **se moviera al revés**, pues el cuadrado verde (la cabeza) aparecía al final.

---

## 🛠️ **La Versión Modificada**

En esta versión se corrigió que la serpiente **se moviera al revés**, haciendo que, desde un principio, la cabeza (el cuadrado verde fuerte) estuviera hasta el final de la cola. Así, cuando la serpiente comía, se creaba una nueva comida y se utilizaba un `enqueue` para añadir al final de la cola la nueva cabeza. 

Pero si la serpiente no ha comido, se realizaba un `dequeue` para eliminar un segmento del cuerpo de la serpiente y también un `enqueue` para añadir la nueva cabeza, de modo que la serpiente **se moviera correctamente**.
