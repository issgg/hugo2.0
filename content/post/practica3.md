---
title: "Práctica: Instalación y uso de Haskell para aplicación TODO"
date: 2025-10-10
summary: "Guía paso a paso para instalar el entorno Haskell y desarrollar una aplicación TODO desde cero utilizando Stack en Windows."
tags: ["Haskell", "Stack", "Instalación", "Aplicación TODO"]
categories: ["Prácticas"]
type: "post"
authors: ["Israel Gomez Ahumada"]
featured_image: "img/practica3.png"
---

## Archivos Prolog de la práctica

- [Descargar family.pl](/prolog/family.pl)
- [Descargar family_ext.pl](/prolog/family_ext.pl)
- [Descargar family_rec.pl](/prolog/family_rec.pl)
- [Descargar kb1.pl](/prolog/kb1.pl)
- [Descargar kb2.pl](/prolog/kb2.pl)
- [Descargar kb3.pl](/prolog/kb3.pl)

## Introducción
 
Esta práctica describe el proceso de instalación y puesta en marcha del entorno Haskell usando la herramienta GHCup en Windows, así como el desarrollo y ejecución de una aplicación tipo TODO con Stack y configuración personalizada.

## Instalación del entorno Haskell

1. Visitar la página oficial de descargas de Haskell.
2. Usar **GHCup** como herramienta recomendada para instalar todos los componentes necesarios:
   - Compilador **GHC**
   - Intérprete **Hugs**
   - **Haskell Language Server (HLS)**
   - **Stack** (gestor de paquetes y proyectos)
   - **Cabal** (empaquetado y construcción)
3. Descargar GHCup y ejecutar el comando de instalación desde PowerShell no administrado.
4. Instalar las herramientas seleccionadas desde la interfaz de GHCup.
5. Verificar instalación con los comandos:
   - `ghc --version`
   - `stack --version`
   - `cabal --version`
6. Seguir la guía oficial rápida (“Get Started”) y asegurar el funcionamiento básico.

## Preparación y desarrollo de la aplicación TODO

1. Crear un proyecto nuevo con Stack:
stack new todo

text
2. Explorar los archivos principales: 
- `app/Main.hs`: lógica y control principal.
- `src/Lib.hs`: funcionalidades internas.
- `package.yaml`: dependencias y configuración.
3. Editar `package.yaml` para agregar librerías como `dotenv` y `open-browser`.
4. Compilar el proyecto:
stack build

text
5. Ejecutar la aplicación:
stack run

text
6. Interactuar con la aplicación a través de comandos/claves:
- `"añadir tarea"` o `o - número`
- `eliminar tarea` o `l`
- `editar tarea` o `e número`
- `mostrar tarea` o `s número`
- `invertir lista` o `r`
- `limpiar lista` o `c`
- `salir` o `q`

7. Crear un archivo `.env` para variables como URL, que pueden abrirse desde la app con comandos personalizados.

## Conclusión

La instalación y uso de Haskell en Windows mediante GHCup y Stack facilita la gestión de entorno y dependencias, permitiendo una experiencia de desarrollo cómoda y productiva para proyectos funcionales como la aplicación TODO. El flujo de trabajo propuesto permite experimentar tanto la construcción como la modularidad típica de Haskell.
