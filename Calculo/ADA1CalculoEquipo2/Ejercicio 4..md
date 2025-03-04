**Enunciado del problema:** Expresar el siguiente enunciado en lenguaje matemático, estableciendo las ecuaciones, conjuntos o inecuaciones que se requieren para resolver el problema: 

Partiendo al medio día, el aeroplano _A_ vuela hacia el norte a la velocidad constante de 650 Km/h. Una hora mas tarde, el aeroplano _B_ vuela hacia el este a la velocidad constante de 490 Km/h. Despreciando la curvatura de la Tierra y suponiendo que vuelan a la misma altura, encuentre una formula para $D(t)$, la distancia entre los dos aviones $t$ horas después del medio día. 

Sabemos por el enunciado que el aeroplano _A_ recorre 650 km en una hora. Por lo que podemos representar la distancia recorrida del aeroplano de la siguiente manera:

$D_{A}(t) = 650t \\\ siendo \\\ t \geq 0$

Ahora por el otro lado sabemos que el aeroplano _B_ recorre 490 km en un hora, sin embargo, este aeroplano despega una hora después del _A_, por lo tanto la formula que representa su distancia recorrida.

$D_{B}(t) = 490(t-1) \\\ siendo \\\ t \geq 1$

$t - 1$ viene a que el aeroplano _B_ despega después de una hora

Ahora debemos aplicar el Teorema de Pitágoras $a^2 + b^2 = c^2$ siendo $a = 650t$ y $b = 490(t-1)$. 

Para ejemplificar lo descrito tenemos la siguiente figura.


```tikz
\usepackage{tikz-cd}
\begin{document}
	\begin{tikzpicture}
		\draw (0,0) node[anchor=north]{$A$}
		  -- (-4,0) node[anchor=north]{$C$}
		  -- (-4,8) node[anchor=south]{$B$}
		  -- cycle;
		\draw[<->] (0,-0.5) -- (-4, -0.5) node[midway, below] {b};
		\draw[<->] (-4.5, 0) -- (-4.5, 8) node[midway, left] {a};
		\draw[<->] (0.5, 0) -- (-4, 8.9) node[midway, above] {c};
	\end{tikzpicture}
\end{document}
```

Reemplazamos los valores en la ecuación.

$(650t)^2 + (490(t - 1))^2 = c^2$


Sacamos raíz cuadrada a ambos lados de la igualdad 

$\sqrt{ (650t)^2 + (490(t - 1))^2 } = c$

Ahora bien podemos representar $c$ como $D(t)$ siendo esta la distancia entre los aviones al pasar de las horas

$D(t) =\sqrt{ (650t)^2 + (490(t - 1))^2 }$

