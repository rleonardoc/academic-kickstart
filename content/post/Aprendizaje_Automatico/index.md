---
date: 2019-10-28T13:17:00
title: Fundamentos de Aprendizaje Automático
summary: Recursos para el curso
authors: ["admin"]
featured: true
event:
image:
  placement: 1
  caption: ""
  focal_point: "Center"
  preview_only: false
markup: mmark
math: true
---

## Notas de clase

+ [Fundamentos de Aprendizaje Automático - Impartido por Pedro Aguilar](seminario3.pdf)

## Tareas seleccionadas

+ [Tarea 1](tarea1.pdf)
+ [Tarea 2](tarea2.pdf)
+ [Tarea 3](tarea3.pdf)

## VC dimension

El manejo de la complejidad de una clase de hipótesis $\mathcal{H}$ requiere de un balance delicado dadas sus amplias repercusiones en los tiempos de compilación de los algoritmos y la capacidad de clasificar fielmente a las observaciones. Por ende, es necesario cuantificar la capacidad con la que $\mathcal{H}$ se adapta a cada conjunto $\mathcal{X}$ y distribución $D$ del cual se obtiene la muestra para entrenar. Las anotaciones de las observaciones $x_{i}$ toman el rol de las posibles combinaciones de posibilidades; por ende, ser capaz de replicar estas variaciones depende de la complejidad de la clase $\mathcal{H}$. 

La restricción de $\mathcal{H}$ a $C = \{ c_{1},\dots,c_{m} \}$ se define como

$$\mathcal{H}_{C} = \{ h(c_{1}),\dots,h(c_{m}) : h \in \mathcal{H} \}$$

Asimismo, se dice que un conjunto $C\subset \mathcal{X}$ es $\textbf{roto}$ por $\mathcal{H}$ si la restricción de $\mathcal{H}$ con $C$ coincide con las posibles funciones $f:C \rightarrow \{ 0,1 \}$. Es decir, los elementos de $\mathcal{H}$ son lo suficientemente variados para describir totalmente cualquier configuración de anotaciones de los elementos de $C$.

Por el momento se han definido conjuntos de muestras que son totalmente explicados – aprendidos – por una clase de hipótesis. Sin embargo, conforme incremente la cardinalidad de $C$, explicar tales variaciones representa un problema para $\mathcal{H}$, dado que esta debe de contener clasificadores aún más específicos. En particular, la cantidad de funciones que la restricción de $\mathcal{H}$ a $C$ debe tener coincide con $2^{|C|}$. Este incremento exponencial de clases de hipótesis limita a $\mathcal{H}$ en el sentido de explicar en su totalidad a los subconjuntos de $\mathcal{X}$. Por supuesto, dados incrementos discretos en la cardinalidad de $C$, debe existir un entero máximo que represente el número de observaciones que, en conjunto, son rotos por $\mathcal{H}$. A esto se le conoce como la dimensión de Vapnik-Chervonenkis, o $VC\dim$ de $\mathcal{H}$.

$$VC\dim(\mathcal{H}) = |C|$$

tal que $C$ es el conjunto de cardinalidad mayor roto por $\mathcal{H}$. La relevancia de este concepto que cuantifica la capacidad de una clase de hipótesis por aprender en su totalidad a un conjunto de cardinalidad $m$ se relaciona directamente con el concepto de aprendizaje PAC. En particular, si $\mathcal{H}$ es una clase cuya dimensión VC es infinita, entonces $\mathcal{H}$ no es PAC aprendible. Otro resultado interesante se encuentra en el teorema fundamental del aprendizaje estadístico, el cual establece la equivalencia entre los siguientes enunciados:

+ $\mathcal{H}$ tiene dimensión VC finita.
+ $\mathcal{H}$ tiene la propiedad de convergencia uniforme.
+ $\mathcal{H}$ es PAC-agnóstico aprendible.
+ $\mathcal{H}$ es PAC aprendible.

### Bibliography

+ Understanding Machine Learning - Shalev-Shwartz, Ben-David.