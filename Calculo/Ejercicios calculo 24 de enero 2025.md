
Ejercicio 4

Encuentra $(a+b)^2$, $a= Senx$
				$b = Cosx$

$a^2 + 2ab + b^2 = (a+b)^2$

Hipotesis: $(a+b)^2$
Tesis: $a^2+2ab+b^2$


Si sabemos que $a^2 = a \cdot a$ entonces $(a+b)^2= (a+b) \cdot (a+b)$. 


| Hechos                                                                                                                  | Justificacion                                            |
| ----------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| $\exists a \in \mathbb{R} \ \wedge \  \exists n \in \mathbb{N}$  $a^n=\underbrace{a \cdot a\cdot \dots a.}_{n \ veces}$ | Definicion de potencia.                                  |
| $a^2=a \cdot a$                                                                                                         | Aplicamos la definicion con $n = 2$.                     |
| $(a+b)^2 = (a+b) \cdot (a+b)$                                                                                           | Definición de exponente 2 en el binomio $(a+b)$.         |
| $(a+b) \cdot (a+b) = a(a+b)+ b(a+b)$.                                                                                   | Propiedad distributiva.                                  |
| $(a+b)^2= a \cdot a + a \cdot b + b \cdot a+ b \cdot b$                                                                 | Propiedad distributiva en $a(a+b)+ b(a+b)$.              |
| $(a+b)^2= a^2 + a\cdot b + b\cdot a + b^2$                                                                              | Aplicando propiedad $a^2= a \cdot a$ y $b^2= b \cdot b$. |
| $(a+b)^2= a^2 + ab + ab + b^2$                                                                                          | Conmutativa $ab = ba$.                                   |
| $(a+b)^2= a^2 + (ab + ab) + b^2$                                                                                        | Asociativa.                                              |
| $\exists \ 1 \in \mathbb{R} \ni x \cdot 1 = 1 \cdot x = x$                                                              | Existencia de elementos neutros de la multiplicacion.    |
| $(a+b)^2= (1)a^2 + ((1)ab + (1)ab) + (1)b^2$                                                                            | Introducción del neutro multiplicativo.                  |
| $(a+b)^2= (1)a^2 + ((1+1)ab) + (1)b^2$                                                                                  | Distributiva en $(1)ab + (1)ab$.                         |
| $(a+b)^2= (1)a^2 + ((2)ab) + (1)b^2$                                                                                    | Suma de $(1+1)ab$ a $2ab$.                               |
| $(a+b)^2= a^2 + (2ab) + b^2$                                                                                            | Existencia de elementos neutros de la multiplicación.    |
| $(a+b)^2= a^2 + 2ab + b^2$                                                                                              | Expresión final                                          |

Hipotesis: $\exists a, b \in \mathbb{R} \ni (a+b)^2$

Tesis: $(a+b)^2 = a^2 + 2ab+ b^2$

| Hechos                                     | Justificacion                                                                       |
| ------------------------------------------ | ----------------------------------------------------------------------------------- |
| $(a+b)^2$                                  |                                                                                     |
| $a^2 +2ab +b^2$                            | Aplicamos la equivalencia de $(a+b)^2 = a^2 + 2ab + b^2$                            |
| $(\sin x)^2+2(\sin x)(\cos x)+ (\cos x)^2$ | Reemplazamos los valores de $a = \sin x$ y $b = \cos x$                             |
| $\sin^2x + 2(\cos x)(\cos x)+\cos^2x$      | Sabemos que $\sin^2x = (\sin x)^2$ y $\cos^2x = (\cos x)^2$                         |
| $2(\sin x)(\cos x)+\cos^2x + \sin^2x$      | Aplicamos la conmutativa en $\sin^2x$                                               |
| $2(\sin x)(\cos x)+\sin^2x+\cos^2x$        | Aplicamos la conmutativa en $\cos^2x$                                               |
| $2(\sin x)(\cos x) + (\sin^2x + \cos^2x)$  | Asociativa en $\sin^2x + \cos^2x$                                                   |
| $2(\sin x)(\cos x)+(1)$                    | Aplicamos identidad trigonometrica de $\sin^2x + \cos^2x = 1$                       |
| $\sin(2x) + 1$                             | Aplicamos identidad trigonometrica de angulos dobles $\sin(2x) = 2(\sin x)(\cos x)$ |


La prueba donde nos piden elementos unicos, la primera es existencia y la segunda es unicidad. La existencia se demuestra dando un candidato y demostrando la propiedad, y la existencia se demuestra dando dos elementos que cumplen la propiedad y demostrando que son iguales.
