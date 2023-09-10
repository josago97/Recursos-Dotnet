# Guía de C#

## Índice

1. [Tipos de datos](#1-tipos-de-datos)

<br>

## 1. Tipos de datos

C# es un lenguaje de tipado **fuerte** y **estático**. A diferencia de otros lenguajes de tipado más débil, en C# cada variable tiene su tipo (con sus correspondientes operaciones definidas) y existen restricciones a la hora de combinar dichos tipos de datos cuando se operan con ellos. 
En un lenguaje de tipado fuerte cuando se usan tipos distintos en una operación no soportada se produce un error en vez de realizarse transformaciones implícitas de datos.

Ejemplo:

JavaScript

```javascript
console.log(2 * "3")
6

console.log([] + {})
'[object Object]'

console.log({} + [])
0
```

C#

```cs
Console.WriteLine(2 * "3");
Error compilación CS0019: Operador '*' no puede ser aplicado a operandos de tipo 'int' y 'string'
```

C# es **estático** porque el el tipo de las variables se define durante la compilación y, por tanto, una variable no puede albergar un dato que no corresponda a su tipo.
<!---
```cs
int numero = 10;
numero = "hola";
Error compilación CS0029: No se puede convertir implícitamente el tipo 'string' a 'int'
```
HABLAR DE LA CONVERSIÓN IMPLICITA

```python
>>> house = 5
>>> house
5
>>> type(house)
<class 'int'>
>>> house = 'hello'
>>> house
'hello'
>>> type(house)
<class 'str'>
```

![types_diagram.png](resources/types_diagram.png)
-->
<br>

### 1.1. Tipos más usados

```CS
int number = 5  // Número entero de 32 bits
float number = 5.1f  // Número real de coma flotante de 32 bits
double number = 5.1  // Número real de coma flotante de 64 bits
bool condition = true  // Booleano (true/false)
char character = 'a' // Carácter
string name = "hello"  // Cadena de texto
name = (1, 2, 'bye')  # tuple
name = [1, 2, 'bye']  # list
name = {1, 2, 'bye'}  # set
name = {1: 2, 'hello': 'world', 'a': 48.34, 48.34: 'a'}  # dictionary
```

<!-- ![collections.png](resources/collections.png)-->

<br>

### 1.2. Conversión de tipos
