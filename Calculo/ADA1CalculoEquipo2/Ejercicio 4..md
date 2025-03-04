**Enunciado del problema:** Expresar el siguiente enunciado en lenguaje matemático, estableciendo las ecuaciones, conjuntos o inecuaciones que se requieren para resolver el problema: 

Partiendo al medio día, el aeroplano _A_ vuela hacia el norte a la velocidad constante de 650 Km/h. Una hora mas tarde, el aeroplano _B_ vuela hacia el este a la velocidad constante de 490 Km/h. Despreciando la curvatura de la Tierra y suponiendo que vuelan a la misma altura, encuentre una formula para $D(t)$, la distancia entre los dos aviones $t$ horas después del medio día. 

Suponiendo que ambos aeroplanos despegan del mismo lugar podemos decir que cuando el aeroplano _B_ el aeroplano _A_, ya ha recorrido 650km.


y en dos horas el aeroplano _A_ habra recorrido 1300 km, y el aeroplano _B_ 490km con esta informacion podemos aplicar el teorema de pitagoras $a^2 + b^2 = c^2$ siendo $a = 1300$ y $b = 490$

```tikz
\documentclass{article}
\usepackage{tikz}
\begin{document}
\begin{tikzpicture}
\draw[gray, thick] (-1,2) -- (2,-4);
\draw[gray, thick] (-1,-1) -- (2,2);
\filldraw[black] (0,0) circle (2pt) node[anchor=west]{Intersection point};
\end{tikzpicture}
\end{document}

```

