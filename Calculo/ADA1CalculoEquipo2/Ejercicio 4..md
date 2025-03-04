**Enunciado del problema:** Expresar el siguiente enunciado en lenguaje matemático, estableciendo las ecuaciones, conjuntos o inecuaciones que se requieren para resolver el problema: 

Partiendo al medio día, el aeroplano _A_ vuela hacia el norte a la velocidad constante de 650 Km/h. Una hora mas tarde, el aeroplano _B_ vuela hacia el este a la velocidad constante de 490 Km/h. Despreciando la curvatura de la Tierra y suponiendo que vuelan a la misma altura, encuentre una formula para $D(t)$, la distancia entre los dos aviones $t$ horas después del medio día. 

Suponiendo que ambos aeroplanos despegan del mismo lugar podemos decir que cuando el aeroplano _B_ el aeroplano _A_, ya ha recorrido 650km.


y en dos horas el aeroplano _A_ habra recorrido 1300 km, y el aeroplano _B_ 490km con esta informacion podemos aplicar el teorema de pitagoras $a^2 + b^2 = c^2$ siendo $a = 1300$ y $b = 490$

```tikz 
\usepackage{tikz-cd} \begin{document} \begin{tikzcd}     T     \arrow[drr, bend left, "x"]     \arrow[ddr, bend right, "y"]     \arrow[dr, dotted, "{(x,y)}" description] & & \\     K & X \times_Z Y \arrow[r, "p"] \arrow[d, "q"]     & X \arrow[d, "f"] \\     & Y \arrow[r, "g"]     & Z \end{tikzcd} \quad \quad \begin{tikzcd}[row sep=2.5em] A' \arrow[rr,"f'"] \arrow[dr,swap,"a"] \arrow[dd,swap,"g'"] &&   B' \arrow[dd,swap,"h'" near start] \arrow[dr,"b"] \\ & A \arrow[rr,crossing over,"f" near start] &&   B \arrow[dd,"h"] \\ C' \arrow[rr,"k'" near end] \arrow[dr,swap,"c"] && D' \arrow[dr,swap,"d"] \\ & C \arrow[rr,"k"] \arrow[uu,<-,crossing over,"g" near end]&& D \end{tikzcd} \end{document} ```
```tikz
\usepackage{tikz-cd} \begin{document} \begin{tikzcd}     T     \arrow[drr, bend left, "x"]     \arrow[ddr, bend right, "y"]     \arrow[dr, dotted, "{(x,y)}" description] & & \\     K & X \times_Z Y \arrow[r, "p"] \arrow[d, "q"]     & X \arrow[d, "f"] \\     & Y \arrow[r, "g"]     & Z \end{tikzcd} \quad \quad \begin{tikzcd}[row sep=2.5em] A' \arrow[rr,"f'"] \arrow[dr,swap,"a"] \arrow[dd,swap,"g'"] &&   B' \arrow[dd,swap,"h'" near start] \arrow[dr,"b"] \\ & A \arrow[rr,crossing over,"f" near start] &&   B \arrow[dd,"h"] \\ C' \arrow[rr,"k'" near end] \arrow[dr,swap,"c"] && D' \arrow[dr,swap,"d"] \\ & C \arrow[rr,"k"] \arrow[uu,<-,crossing over,"g" near end]&& D \end{tikzcd} \end{document}
```
