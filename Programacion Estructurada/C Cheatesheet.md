# C Cheatsheet
---
## Sintaxis Básica

- **`#include <stdio.h>:`** Es una librería que va en el encabezado que nos da algunas funciones estándar como **`printf`** y **`scanf`**.
- **`int main()`**: La función `main()` es punto de entrada de cualquier programa de C, es decir, cualquier cosa que se encuentre dentro de los `{ }`.
- **`printf()`:** La función `printf()` se usa para imprimir una salida o texto en la terminal.
- **`return 0`:** Termina la función `main ()` .

Un ejemplo de la sintaxis básica es el siguiente: 

```c
#include <stdio.h>

int main(){
	printf("Hello World");
	return 0;
}
```
---
## Palabras reservadas en C
---

- `int`:
- `long`:
- `short`:
- `signed`:
- `unsigned`:
- `void`:
- `char`:
- `break`:
- `register`:
- `structure`:
- `class`: 
- `volatile`:
- `while`:
- `for`:
- `switch`:
- `typedef`:
- `union`:
- `static`:
- `auto`:
- `return`:
- `case`:
- `const`:
- `continue`:
- `default`:
- `do`:
- `double`:
- `else`:
- `if`:
- `enum`:
- `extern`:
- `float`:
- `goto`:
---
## Variables de C
---

Las tipos de variables que tiene de manera predeterminada C son:

- **int:** Almacena numeros enteros.
- **float:** Almacena números flotantes, es decir, números decimales con una precisión de hasta 6 - 7 decimales.
- **double:** Almacena números decimales hasta con una precisión de 15 decimales.
- **char:** Almacena un solo carácter.

Ejemplos:

```C
char caracter = 'a';
int entero = 24;
float decimal = 24.32;
double decimalDoble = 24.3435;
```

Para imprimir una variable usando la función `printf()` se necesita usar un especificador de formato. 

| Especificador de formato |        Nombre        |
|:------------------------:|:--------------------:|
|            %c            |       Caracter       |
|            %d            |    Numero entero     |
|            %f            |  Numero decimal (6)  |
|           %lf            | Numero decimal (15)  |
|            %s            | Cadena de caracteres |

---
## Arreglos
---
Los arreglos sirven para almacenar varias valores en una sola variable. La estructura de los arreglos es la siguiente:

```C
int nombre_variable [] = {2, 3, 4, ...};
```

En la primera parte del código definimos el tipo de variables que se van a almacenar dentro del arreglo. Ahora bien para imprimir algún elemento almacenado en el arreglo necesitamos especificar la posición en la que se encuentra ese valor. Ejemplo:

```C
int nombre_varible [] = {2,3,4};
printf("%d", nombre_variable[2]);

// imprime el numero: 4
```

La primera posición del arreglo siempre es `0`. Para cambiar el valor de un elemento de un arreglo es necesario nombrar al arreglo y especificar la posición que queremos cambiar. 

```C
int nombre_varible [] = {2,3,4};
printf("%d", nombre_variable[2]);

// imprime el numero: 4

nombre_variable [2] = 6;
printf("%d", nombre_variable[2]);

//imprime el numero: 6
```


Para hacer recorrer todos los valores de un arreglo, necesitamos usar un ciclo `for`.

```C
int nombre_varible [] = {2,3,4,5,6};

for(int i = 0; i <= 4, i++){
	printf("%d \n", nombre_variable[i]);
}
```

Una practica común es definir el tamaño del arreglo y posteriormente agregar elementos.

```C
int nombre_variable [5];

nombre_variable [0] = 1;
nombre_variable [1] = 2;
nombre_variable [2] = 3;
nombre_variable [3] = 4;
nombre_variable [4] = 5;
nombre_variable [5] = 6;
```

Se pueden definir definir arreglos de mas de una dimensión y para hacer esto se debe especificar en el arreglo. Ejemplo:

```C
int nums[2][3] = {{1,2,3}{4,5,6}};
```

Esto se veria de la siguiente manera


|        | columna 0 | columna 1 | columna2 |
| ------ | --------- | --------- | -------- |
| fila 0 | 1         | 2         | 3        |
| fila 1 | 4         | 5         | 6        |


Y para acceder al elemento se especifica la posicion.

```C
int nums[2][3] = {{1,2,3}{4,5,6}};
printf("%d", nums[0][2]);

//imprime el numero: 3
```

#### Cadenas de caracteres 

Para poder almacenar una cadena de caracteres `string` en C, debemos usar el tipo de variable `char` y almacenar todo en un arreglo. Y para imprimirlo se usa `"%s"`.

```C
char mensaje[] = {"Hola mundo"};
pritf("%s", mensaje);
```

Otra de las cosas que podemos hacer con esto es que podemos acceder a la posición de un carácter de la `string`.

```C
char mensaje[] = {"Hola mundo"};
pritf("%s", mensaje[0]);

//Imprime el caracter 'H'
```

---
## Operadores de C
---

#### Operadores Aritmeticos


| Operador |     Nombre      |
|:--------:|:---------------:|
|    +     |      Suma       |
|    -     |      Resta      |
|    *     | Multiplicacion  |
|    /     |    Division     |
|    %     |     Modulo      |
|    ++    | Incremento en 1 |
|    --    | Decremento en 1 |

#### Operadores Relacionales

| Operador |      Nombre       |
|:--------:|:-----------------:|
|    ==    |     Es igual      |
|    !=    |    No es igual    |
|    >     |     Mayor que     |
|    <     |     Menor que     |
|    >=    | Mayor o igual que |
|    <=    | Menor o igual que |

#### Operadores Logicos

| Operador | Nombre |
|:--------:|:------:|
|    &&    |  AND   |
|  \| \|   |   OR   |
|    !     |  NOT   |

---
## Estructuras de control de C

---

#### Estructura `if`

La estructura contiene un bloque de codigo que se ejecutara unicamente si la condicion es verdadera.


```C
if (condicion){
	//Codigo
}
```

#### Estructura `if-else`

La estructura `if-else` es similar a la de `if` pero con la adición de `else` después de las llaves de `if` que ejecutara un código en el caso de que la condición de el `if` sea falsa.

```C
if (condicion){
	//Codigo
} else {
	//Codigo
}
```

#### Estructura `if-else-if`

La estructura `if-else-if` sirve para cuando quieres comprobar ciertas condiciones si la condición inicial del `if` es falsa, además de que esta tiene un código que se ejecuta si la condición es verdadera.

```C
if (condicion1){
	//Codigo
}else if (condicion2){
	//Codigo
}else{
	//Codigo
}
```

#### Estructura `switch case`

La estructura `switch-case` es una alternativa a la estructura `if-else-if`, esta estructura elige un `case` que cumpla con el valor de una sola variable. Este no se recomienda para condiciones complejas.

```C
switch(variable){
	case valor1:
		//Codigo
		break;
	case valor2:
		//Codigo
		break;
	default:
		//Codigo en caso de que no cumpla con ningun valor
		break;
}
```

#### Estructura operador condicional 

El operador condicional es una sola linea de un `if-else` que revisa si la condición es verdadera ejecuta una código, y en dado caso que sea falso ejecuta otro código.

```C
(condicion) ? (expresion_verdadera) : (expresion_falsa);
```

```C
(int i = 5 < 10) ? (printf("i es menor que 10")) : (printf("i es mayor que 10"));

//La salida seria "i es menor que 10"
```

#### Estructura para ciclo `for`

El ciclo `for` esta compuesto por tres partes inicialización, condición y actualización.

```C
for (inicializacion; condicion; actualizacion){
	//Codigo
}
```

#### Estructura para el ciclo `while`

El ciclo `while` esta compuesto solamente por una condición. Sin embargo normalmente se hace una variable externa que será modificada dentro del ciclo hasta que la condición sea falsa.

```C
int i = 0;

while (condicion){
	//Codigo
	i++;
} 
```

#### Estructura para el ciclo `do-while`

El ciclo `do-while` es un ciclo en el cual la condición es revisada después del código del ciclo.

```C
do {
	//Codigo
} while (condicion);
```
---
## Bibliotecas mas populares de C
---

Las funciones de la biblioteca `stdio.h`

|   Función    |                                                                  Descripción                                                                  |
|:------------:|:---------------------------------------------------------------------------------------------------------------------------------------------:|
|  `fclose()`  |                                                               Cierra un archivo                                                               |
|   `feof()`   |               La rutina `feof` (que se implementa como función y como macro) determina si se ha superado el final de `stream`.                |
|  `ferror()`  |           Si no se ha producido ningún error en `stream`, `ferror` devuelve 0. De lo contrario, devuelve un valor distinto de cero.           |
|  `fgetc()`   |                   `fgetc` devuelve el carácter leído como `int` o devuelve EOF para indicar un error o el final de archivo.                   |
|  `fgets()`   |                                        Lee una linea de un archivo y avanza la función del indicador.                                         |
|  `fopen()`   |                              Devuelve un puntero al archivo abierto. Un valor de puntero `null` indica un error.                              |
| `fprintf()`  |                          `fprintf` da formato e imprime una serie de caracteres y valores en la salida de `stream`.                           |
|  `fputc()`   |                                            Devuelve un carácter y avanza de posición el indicador.                                            |
|  `fputs()`   |                                     Devuelve una cadena de caracteres y avanza de posición el indicador.                                      |
|  `fread()`   |                                      Lee información de un archivo y lo escribe en un bloque de memoria.                                      |
|  `fscanf()`  |                                `fscanf` es utilizada para leer datos de un archivo de un formato especificado.                                |
|  `fseek()`   |                    `fseek` se utiliza para mover el puntero de posición en un archivo abierto a una ubicación específica.                     |
|  `ftell()`   |                                  `ftell` se utiliza para obtener la posición actual del puntero del archivo.                                  |
|  `fwrite()`  |                           `fwrite` se utiliza para escribir datos binarios desde un bloque de memoria a un archivo.                           |
|   `getc()`   |                                            Lo mismo que `fgetc`, la diferencia es de optimización.                                            |
| `getchar()`  |                                  `getchar()` lee un carácter de entrada de usuario y retorna su valor ASCII                                   |
|  `printf()`  |                                             `printf()` imprime un texto formateado en la consola.                                             |
|   `putc()`   |                                            Lo mismo que `fputc`, la diferencia es de optimización.                                            |
| `putchar()`  |                                              `putchar()` imprime un solo carácter en la consola.                                              |
|   `puts()`   |                                           `puts()` imprime una cadena de caracteres en la consola.                                            |
|  `remove()`  |                                                        `remove()` elimina un archivo.                                                         |
|  `rename()`  |                                                   `rename()` cambia el nombre del archivo.                                                    |
|  `rewind()`  |                                      `rewind()` mueve de posición del indicador al inicio del archivo.                                       |
|  `scanf()`   |            `scanf()` lee información formateada de la entrada del usuario y lo escribe en un numero de localizaciones de memoria.             |
| `snprintf()` |         `snprintf()` escribe una cadena de caracteres formateada en un arreglo de caracteres `char` (es mas seguro que `sprintf()`).          |
| `sprintf()`  |                          `sprintf()` escribe una cadena de caracteres formateada en un arreglo de caracteres `char`.                          |
|  `sscanf()`  | `sscanf()` lee una cadena de caracteres formateada de un arreglo de caracteres `char` y lo escribe en un numero de localizaciones de memoria. |


Otra de las bibliotecas mas populares `stdlib.h`.


|   Función   |                                                                       Descripción                                                                       |                         Algunas sintaxis                          |
|:-----------:|:-------------------------------------------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------:|
|   `abs()`   |                                                     Retorna el numero absoluto de un numero entero                                                      |                                                                   |
|  `atof()`   |                                Retorna un valor `double` de una representación de un numero en una cadena de caracteres                                 |                                                                   |
|  `atoi()`   |                                  Retorna un valor `int` de una representación de un numero en una cadena de caracteres                                  |                                                                   |
|  `atol()`   |                               Retorna un valor `long int` de una representación de un numero en una cadena de caracteres                                |                                                                   |
|  `atoll()`  |                             Retorna un valor `long long int` de una representación de un numero en una cadena de caracteres                             |                                                                   |
| `calloc()`  |                         Se utiliza para asignar memoria dinámica para un numero especifico de elementos llenándolos con ceros.                          |   `calloc(numero_de_elementos, tamano_de_cada elemento_bytes);`   |
|   `div()`   |                                              Retorna el cociente y el residuo de una división de enteros.                                               |                `div(int dividendo, int divisor);`                 |
|  `exit()`   |                                                                   Termina el programa                                                                   |                                                                   |
|  `free()`   |                                Libera memoria asignada dinámicamente mediante funciones `malloc`, `calloc` o `realloc`.                                 |                      `free(void * pointer);`                      |
| `malloc()`  |                                    Se utiliza para asignar memoria dinámica para un numero especifico de elementos.                                     |                                                                   |
|  `qsort()`  |                                            Función que ordena de menor a mayor los elementos de un arreglo.                                             | `qsort(array, number_elements_array, size_element_array, compar)` |
|  `rand()`   |                                                         Genera aleatoriamente un numero entero                                                          |                                                                   |
| `realloc()` |                                   Cambia el tamaño de un bloque de memoria y retorna un puntero al bloque de memoria.                                   |                    `realloc(ptr, size_bytes);`                    |
|  `srand()`  | La función `srand` para inicializar la semilla del generador de números pseudoaleatorios. Se usa junto de `rand()` para generar números mas aleatorios. |                    `srand(unsigned int seed);`                    | 
Funciones de la librería `<math.h>`



|     Función      |                                               Descripción                                                |
|:----------------:|:--------------------------------------------------------------------------------------------------------:|
|    `acos(x)`     |                                   Retorna el arcoseno de x en radianes                                   |
|    `acosh(x)`    |                                    Retorna el coseno hiperbólico de x                                    |
|    `asin(x)`     |                                     Retorna arcoseno de x en radianes                                     |
|    `asinh(x)`    |                                     Retorna el seno hiperbólico de x                                     |
|    `atan(x)`     |                        Retorna el Arc tangente de x en un numero entre -𝜋/2 y 𝜋/2                         |
|   `atan2(y,x)`   | Retorna el ángulo θ de la conversión de las coordenadas rectangulares (x,y) a coordenadas polares (r, θ) |
|    `cbrt(x)`     |                                       Retorna el valor cubico de x                                       |
|    `ceil(x)`     |                     Retorna el valor de x redondeado a su numero entero mas cercano.                     |
| `copysign(x, y)` |                  Retorna el primer numero flotante x con el signo del segundo numero y.                  |
|     `cos(x)`     |                                    Retorna el coseno de x en radianes                                    |
|    `cosh(x)`     |                                    Retorna el coseno hiperbólico de x                                    |
|     `exp(x)`     |                         Retorna el valor del numero de $e$ (Euler) elevado $e^x$                         |
|    `exp2(x)`     |                                        Retorna el valor de $2^x$                                         |
|    `expm1(x)`    |                                        Retorna el valor $e^x -1$                                         |
|     `log(x)`     |                                    Retorna el logaritmo natural de x                                     |
|    `log10(x)`    |                                    Retorna logaritmo con base 10 de x                                    |
|    `pow(x,y`     |                                 Retorna el valor de `x` elevado a la `y`                                 |
|     `sin(x)`     |                                    Retorna el seno de `x` en radianes                                    |
|    `sinhx(x)`    |                                     Retorna el seno hiperbólico de x                                     |
|    `sqrt(x)`     |                                     Retorna la raíz cuadrada de `x`                                      |
|     `tan(x)`     |                                  Retorna la tangente de `x` en radianes                                  |
|    `tanh(x)`     |                                  Retorna el tangente hiperbólica de `x`                                  |


## Funciones de entrada y salida

### Salida

Las funciones de salida mas de la librería `<stdio.h>` 


#### `printf()`

`printf()` imprime un texto formateado en la consola.

```C
int main(){ 
	printf("Hola mundo\n"); 
	printf("Número entero: %d, Número flotante: %.4f\n", 42, 3.1416); 
	return 0; 
}
```

#### `putchar()`

`putchar()` imprime un solo carácter en la consola.
```C
int main() {
    putchar('A');
    putchar('\n');
    return 0;
}
```
#### `puts()`

`puts()` imprime una cadena de caracteres en la consola seguida de un salto de linea.
```C
int main() {
    puts("Hola, mundo!");
    return 0;
}
```

### Entrada

#### `scanf()`

 `scanf()` lee información formateada de la entrada del usuario y lo escribe en un numero de localizaciones de memoria. 
```C
int main() {
    int numero;
    printf("Introduce un numero entero: ");
    scanf("%d", &numero);
    printf("El numero ingresado es: %d\n", numero);
    return 0;
}
```

#### `getchar()`

`getchar()` lee un carácter de entrada de usuario y retorna su valor ASCII.

```C
int main() {
    char c;
    printf("Introduce un carácter: ");
    c = getchar();
    printf("El carácter ingresado es: %c\n", c);
    return 0;
}
```

#### `gets()`

```C
int main() {
	char str[5];
	printf("Escribe una cadena de caracteres");
	gets(str);
	printf("La cadena de caracteres es: \n");
	puts(str);
}
```

## Ejemplos

Ejemplo de imprimir si el numero es par o impar.

```C
#include <stdio.h>

int main(){
    int number;
    
    printf("Ingresa un numero \n");
    scanf("%d", &number);
    if ((number % 2) == 0){
        printf("Es par");
    } else {
        printf("Es impar");
    }
    return 0;
}
```

Ejemplo rango de números impar.

```C
#include <stdio.h>

void rangoNumerosImpares(int inicio, int final){

    for (int i = inicio; i < final; i++){
        if (!((i % 2) == 0)){
            printf("%d \n", i);
        }
    }
}

int main(){

    int a, b;

    printf("Escribe el numero inicial de los numeros impares: ");
    scanf("%d", &a);
    printf("Escribe el numero final de los numeros impares: ");
    scanf("%d", &b);
    rangoNumerosImpares(a, b);

}
```

Ejemplo calcular el área de un rectángulo.

```C
#include <stdio.h>

int main() {
  int largo = 4;
  int ancho = 6;
  int area;

  area = largo * ancho;

  printf("El largo es: %d\n", largo);
  printf("El ancho es: %d\n", ancho);
  printf("El area del rectangulo es: %d", area);

  return 0;
}
```