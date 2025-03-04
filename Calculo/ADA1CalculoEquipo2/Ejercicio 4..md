**Enunciado del problema:** Expresar el siguiente enunciado en lenguaje matemático, estableciendo las ecuaciones, conjuntos o inecuaciones que se requieren para resolver el problema: 

Partiendo al medio día, el aeroplano _A_ vuela hacia el norte a la velocidad constante de 650 Km/h. Una hora mas tarde, el aeroplano _B_ vuela hacia el este a la velocidad constante de 490 Km/h. Despreciando la curvatura de la Tierra y suponiendo que vuelan a la misma altura, encuentre una formula para $D(t)$, la distancia entre los dos aviones $t$ horas después del medio día. 

Sabemos por el enunciado que el aeroplano _A_ recorre 650 km en una hora. Por lo que podemos representar la distancia recorrida del aeroplano de la siguiente manera:

$D(t) = 650t \\\ siendo \\\ t \\\ horas$

Ahora por el otro lado sabemos que el aeroplano _B_ recorre 490 km en un hora, sin embargo, este aeroplano despega una hora después del _A_, por lo tanto la formula que representa su distancia recorrida.

$D(t) = 490(t - 1) \\\ siendo \\\ t \\\ horas$

$t - 1$ viene

```tikz 
\usepackage{tikz-cd} \begin{document} \begin{tikzcd}     T     \arrow[drr, bend left, "x"]     \arrow[ddr, bend right, "y"]     \arrow[dr, dotted, "{(x,y)}" description] & & \\     K & X \times_Z Y \arrow[r, "p"] \arrow[d, "q"]     & X \arrow[d, "f"] \\     & Y \arrow[r, "g"]     & Z \end{tikzcd} \quad \quad \begin{tikzcd}[row sep=2.5em] A' \arrow[rr,"f'"] \arrow[dr,swap,"a"] \arrow[dd,swap,"g'"] &&   B' \arrow[dd,swap,"h'" near start] \arrow[dr,"b"] \\ & A \arrow[rr,crossing over,"f" near start] &&   B \arrow[dd,"h"] \\ C' \arrow[rr,"k'" near end] \arrow[dr,swap,"c"] && D' \arrow[dr,swap,"d"] \\ & C \arrow[rr,"k"] \arrow[uu,<-,crossing over,"g" near end]&& D \end{tikzcd} \end{document} ```
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

$(650x)^2 + (490(x - 1))^2 = c^2$


$\sqrt{ (650x)^2 + (490(x - 1))^2 } = c$