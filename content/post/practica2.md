---
title: "Práctica : Migración del Sistema de Biblioteca de C a Python"
date: 2025-10-03
summary: "Reporte sobre la migración de un sistema de biblioteca de C a Python, aplicando conceptos de Programación Orientada a Objetos."
tags: ["C", "Python", "POO", "Paradigmas", "Migración"]
categories: ["Prácticas"]
type: "post"
authors: ["Israel Gomez Ahumada"]
featured_image: "img/practica2.png"
---

## Introducción

En esta práctica se analiza el proceso de migración de un sistema de biblioteca desarrollado en C hacia una versión en Python utilizando Programación Orientada a Objetos (POO). Se estudian los beneficios, retos y diferencias clave entre ambos enfoques.

## Conceptos de Programación Orientada a Objetos

- **Clase:**  
  Una plantilla para definir atributos y métodos comunes. Ejemplo:  
  La clase `Book` en Python tiene atributos como `id`, `title`, `author` y métodos como `todict()`.

- **Objeto:**  
  Instancia concreta de una clase. Por ejemplo, cada libro cargado por el sistema es un objeto `Book`.

- **Herencia:**  
  Permite que una clase hija utilice atributos y métodos de la clase padre. `DigitalBook` hereda de `Book`.

- **Encapsulamiento:**  
  Protege atributos internos de la clase, asegurando que solo sean modificados mediante métodos.

- **Abstracción:**  
  Oculta detalles de implementación mostrando solo lo esencial. Ejemplo: el método `savelibrarytofile()` abstrae el proceso de guardado.

- **Polimorfismo:**  
  Objetos pueden modificar el comportamiento de métodos heredados. Ejemplo: `todict()` es sobrescrito en clases hijas.

## Comparación C vs Python POO

| Característica      | C                                   | Python POO                         |
|---------------------|-------------------------------------|------------------------------------|
| Estructura de datos | structs y listas enlazadas          | Clases y listas nativas de Python  |
| Lógica y operaciones| Funciones globales                  | Métodos de clase                   |
| Manejo de memoria   | Manual, con `malloc` y `free`       | Automático, recolector de basura   |
| Persistencia        | Manual y propenso a errores         | Métodos robustos con JSON          |
| Extensibilidad      | Compleja                            | Sencilla y escalable               |

## Ventajas y conclusiones

La migración a Python y la implementación de POO facilitan la mantenibilidad, legibilidad y reusabilidad del sistema. El encapsulamiento y la herencia permiten proteger y ampliar la lógica sin duplicar código. El manejo automático de memoria y métodos para persistencia de datos reducen los errores y simplifican el desarrollo, logrando un sistema más robusto y escalable.

---
