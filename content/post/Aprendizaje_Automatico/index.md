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

El manejo de la complejidad de una clase de hipótesis $\mathcal{H}$ requiere de un balance delicado dadas sus amplias repercusiones en los tiempos de compilación de los algoritmos y la capacidad de clasificar fielmente a las observaciones. Por ende, es necesario cuantificar la capacidad con la que $\mathcal{H}$ se adapta a cada conjunto $\mathcal{X}$ y distribución $D$ del cual se obtiene la muestra para entrenar. Las anotaciones de las observaciones $x_{i}$ toman el rol de las posibles combinaciones de posibilidades; por ende, ser capaz de replicar estas variaciones depende de la complejidad de la clase $\mathcal{H}$. Asimismo, se dice que un conjunto $C\subset \mathcal{X}$ es \textbf{roto} por $\mathcal{H}$ si la restricción de $\mathcal{H}$ con $C$ coincide con las posibles funciones $f:C \rightarrow \{ 0,1 \}$. 

### Bibliography

+ Understanding Machine Learning - Shalev-Shwartz, Ben-David.