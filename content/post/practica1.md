---
title: "Práctica Elementos fundamentales de los lenguajes de programación"
date: 2025-09-26
summary: "Identificación y explicación de conceptos esenciales en los lenguajes C a partir de los archivos biblioteca.c y memorymanagement.c."
tags: ["C", "Paradigmas", "Lenguajes de Programación"]
categories: ["Prácticas"]
type: "post"
authors: ["Israel Gomez Ahumada"]
featured_image: "img/practica1.PNG"
---

## Introducción

![Portada de la práctica](/img/practica1.png)

El objetivo de esta práctica es identificar los elementos fundamentales de los lenguajes de programación en los archivos `biblioteca.c` y `memorymanagement.c`, analizando cómo se implementan conceptos como nombres, marcos de activación, bloques de alcance, administración de memoria, expresiones, comandos, control de secuencia, subprogramas y tipos de datos.

Repositorio del código: [github.com/gallegosj89/portafolio](https://github.com/gallegosj89/portafolio)

---

## Desarrollo

### 1. Nombres (Identificadores)

En C, los nombres son identificadores que representan variables, funciones, estructuras o constantes.

**Ejemplo del archivo biblioteca.c**

struct Libro {
char titulo;​
char autor;​
int anio;
}

Los nombres como `Libro`, `titulo`, `autor`, `anio`, `agregarLibro`, `mostrarLibros`, `main` permiten referirse a estructuras y funciones.

---

### 2. Marcos de activación (Stack Frames)

Cada vez que se ejecuta una función, se crea un marco de activación en la pila con variables locales y parámetros.

void agregarLibro(struct Libro lista[], int contador) {
struct Libro nuevo;
printf("Ingrese titulo: ");
scanf("%s", nuevo.titulo);
lista[contador] = nuevo;
contador++;
}

Se reserva espacio en la pila para la variable local `nuevo`. Al terminar, el marco se destruye y la pila regresa a su estado anterior.

---

### 3. Bloques de alcance

En C existen variables globales y locales.

struct Libro listaLibros; // Variable global​
int contador = 0; // Variable global

void mostrarLibros() {
for(int i = 0; i < contador; i++) { // Variable local i
printf("%s\n", listaLibros[i].titulo);
}
}

`listaLibros` y `contador`: alcance global.  
`i`: alcance local en la función `mostrarLibros`.

---

### 4. Administración de memoria

En `memorymanagement.c` se ejemplifica la reserva y liberación dinámica de memoria:

int* arr = (int*) malloc(5 * sizeof(int));
if (arr == NULL) {
printf("Error al asignar memoria");
}
for(int i = 0; i < 5; i++) {
arr[i] = i + 1;
}
free(arr);

`malloc` reserva memoria en el heap.  
`free` libera la memoria usada.

---

### 5. Expresiones

Son combinaciones de valores, variables y operadores.

arr[i] = i + 1; // Expresión aritmética
if(anio > 2000) ... // Expresión booleana

`i + 1` es aritmética.  
`anio > 2000` es lógica.

---

### 6. Comandos (Sentencias)

Los comandos son instrucciones que ejecuta el programa.

- `printf("Ingrese titulo");` (salida)
- `scanf("%s", nuevo.titulo);` (entrada)
- `return 0;` (terminación)

---

### 7. Control de secuencia

**Selección:**  
Uso de `if` y `switch` para tomar decisiones.

if(anio > 2000)
printf("Libro moderno");
else
printf("Libro antiguo");

**Iteración:**  
Uso de ciclos `for` y `while`.

for(int i = 0; i < contador; i++)
printf("%s\n", listaLibros[i].titulo);

**Recursión:**  
No aparece en estos archivos, pero típicamente:
int factorial(int n) {
if(n <= 1) return 1;
return n * factorial(n-1);
}

---

### 8. Subprogramas (Funciones)

En C, las funciones permiten modularizar el código.

void mostrarLibros() {
for(int i = 0; i < contador; i++)
printf("%s\n", listaLibros[i].titulo);
}

`mostrarLibros` imprime la lista de libros.

---

### 9. Tipos de datos

Se usan tanto primitivos como compuestos.

- **Primitivos:** `int`, `char`, `float`
- **Compuestos:** `struct Libro`

struct Libro {
char titulo;​
char autor;​
int anio;
}

---

## Conclusión

Se logró identificar de manera práctica los conceptos clave de los lenguajes de programación, facilitando la comprensión de su uso y estructura en C.

---
