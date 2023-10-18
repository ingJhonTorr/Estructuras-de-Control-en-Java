# Estructuras de Control en Java

## Introducción
Las estructuras de control son componentes esenciales en la programación. En Java, se utilizan para tomar decisiones, ejecutar bucles y seleccionar entre múltiples opciones. A continuación, exploraremos las estructuras de control `if`, `switch`, `while` y `for`, junto con ejemplos que destacan su funcionalidad y los operadores que las acompañan.

## Estructura de control `if`

La estructura `if` se utiliza para tomar decisiones basadas en una condición.

### Sintaxis:

```java
if (condición) {
    // Código a ejecutar si la condición es verdadera
}
```

**Operadores Utilizados**:

#### Operadores de Comparación:
- `==`: Igual a (compara si dos valores son iguales).
- `!=`: Diferente de (compara si dos valores no son iguales).
- `<`: Menor que (compara si un valor es menor que otro).
- `>`: Mayor que (compara si un valor es mayor que otro).
- `<=`: Menor o igual que (compara si un valor es menor o igual que otro).
- `>=`: Mayor o igual que (compara si un valor es mayor o igual que otro).

#### Operadores Aritméticos:
- `+`: Suma (realiza una operación de suma).
- `-`: Resta (realiza una operación de resta).
- `*`: Multiplicación (realiza una operación de multiplicación).
- `/`: División (realiza una operación de división).

#### Operadores Booleanos:
- `&&`: Y lógico (realiza una operación lógica "y" entre dos condiciones).
- `||`: O lógico (realiza una operación lógica "o" entre dos condiciones).
- `!`: NO lógico (niega una condición).

### Ejemplo 1:

```java
int edad = 21;

if (edad >= 18) {
    System.out.println("Eres mayor de edad.");
} else {
    System.out.println("Eres menor de edad.");
}
```

**Explicación**:
- En este ejemplo, se utiliza el operador de comparación `>=` para verificar si la variable `edad` es mayor o igual a 18. Si es verdadero, se imprime "Eres mayor de edad."

### Ejemplo 2:

```java
char letra = 'A';

if (Character.isUpperCase(letra)) {
    System.out.println("La letra es mayúscula.");
} else {
    System.out.println("La letra es minúscula.");
}
```

**Explicación**:
- En este ejemplo, se utiliza el método `Character.isUpperCase()` para verificar si `letra` es una letra mayúscula. Si es verdadero, se imprime "La letra es mayúscula."

### Ejemplo 3:

```java
boolean esEstudiante = true;
boolean tieneDescuento = false;

if (esEstudiante && !tieneDescuento) {
    System.out.println("Tienes un descuento de estudiante.");
} else {
    System.out.println("No tienes un descuento de estudiante.");
}
```

**Explicación**:
- En este ejemplo, se utilizan operadores lógicos para combinar condiciones. Se verifica si una persona es estudiante y no tiene un descuento.

## Estructura de control `switch`

La estructura `switch` se utiliza para seleccionar entre múltiples opciones de una expresion.

### Sintaxis:

```java
switch (expresión) {
    case valor1:
        // Código a ejecutar si expresión == valor1
        break;
    case valor2:
        // Código a ejecutar si expresión == valor2
        break;
    // Otros casos...
    default:
        // Código a ejecutar si no coincide con ningún caso
}
```

### Ejemplo 1:

```java
char operador = '+';
int a = 5;
int b = 3;
int resultado = 0;

switch (operador) {
    case '+':
        resultado = a + b;
        break;
    case '-':
        resultado = a - b;
        break;
    default:
        System.out.println("Operador no válido.");
}
System.out.println("Resultado: " + resultado);
```

**Explicación**:
- En este ejemplo, se utiliza el operador de igualdad `==` para comparar `operador` con diferentes casos. El resultado se calcula según el valor de `operador."

## Estructura de control `while`

La estructura `while` se utiliza para repetir un bloque de código mientras una condición sea verdadera.

### Sintaxis:

```java
while (condición) {
    // Código a ejecutar mientras la condición sea verdadera
}
```

### Ejemplo 1:

```java
int contador = 1;
int limite = 5;

while (contador <= limite) {
    System.out.println("Contador: " + contador);
    contador++;
}
```

**Explicación**:
- En este ejemplo, se utiliza el operador de comparación `<=` para verificar si `contador` es menor o igual a `limite`. El bloque de código se ejecuta mientras esta condición sea verdadera.

### Ejemplo 2:

```java
double saldo = 1000.0;
double tasaDeInterés = 0.05;
int años = 5;

while (años > 0) {
    saldo += saldo * tasaDeInterés;
    años--;
}
System.out.println("Saldo después de 5 años: " + saldo);
```

**Explicación**:
- En este ejemplo, se utilizan variables de tipo `double` para representar valores decimales. Se realizan cálculos de interés compuesto durante un período de tiempo.

### Ejemplo 3:

```java
int número = 1;

while (número < 10) {
    System.out.print(número + " ");
    número++;
}
System.out.println();
```

**Explicación**:
- En este ejemplo, se utiliza el operador de comparación `<` para verificar si `número` es menor que 10. Se imprimen los números del 1 al 9 en una línea.

## Estructura de control `for`

La estructura `for` se utiliza para realizar bucles con un contador específico.

### Sintaxis:

```java
for (inicialización; condición; incremento) {
    // Código a ejecutar en cada

 iteración
}
```

### Ejemplo 1:

```java
int suma = 0;

for (int i = 1; i <= 10; i++) {
    suma += i;
}
System.out.println("La suma de los números del 1 al 10 es: " + suma);
```

**Explicación**:
- En este ejemplo, se utiliza el operador de comparación `<=` para verificar si `i` es menor o igual a 10. El contador `i` se incrementa en cada iteración. El operador `+=` se utiliza para acumular la suma de los números del 1 al 10.

### Ejemplo 2:

```java
int factorial = 1;
int n = 5;

for (int i = 1; i <= n; i++) {
    factorial *= i;
}
System.out.println("El factorial de " + n + " es " + factorial);
```

**Explicación**:
- En este ejemplo, se utiliza la estructura `for` para calcular el factorial de un número `n`. Se utiliza el operador `*=` para realizar la multiplicación acumulativa.

### Ejemplo 3:

```java
for (int i = 0; i < 5; i++) {
    for (int j = 0; j < i; j++) {
        System.out.print("* ");
    }
    System.out.println();
}
```

**Explicación**:
- En este ejemplo, se utiliza la estructura `for` anidada para imprimir un patrón de estrellas. El primer bucle controla las filas y el segundo bucle controla las estrellas en cada fila.
