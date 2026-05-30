# Técnicas de Usabilidad - Refactorización Accesible (WCAG 2.1 AA)

Este repositorio contiene el código fuente de una Single Page Application (SPA) sobre Técnicas de Usabilidad. El proyecto ha sido auditado y refactorizado a nivel estructural y de comportamiento para cumplir estrictamente con el **Nivel AA de las directrices WCAG 2.1**, aplicando los principios de Diseño Universal y la normativa LSSICE.

## 🚀 Mejoras de Accesibilidad Implementadas

El proyecto original presentaba barreras críticas de accesibilidad dinámica (un fallo común en arquitecturas SPA). Se han aplicado las siguientes soluciones:

* **Operatividad por Teclado nativa:** Sustitución de contenedores genéricos `<div>` interactivos por elementos `<button>` semánticos.
* **Gestión Asíncrona del Foco:** Implementación de foco dinámico en JavaScript (`.focus()`) combinado con atributos `tabindex="-1"` para guiar a los lectores de pantalla al cargar nuevo contenido, eliminando el "limbo del foco".
* **Estructura Semántica:** Integración de *Landmarks* nativos (`<main>`, `<nav>`, `<header>`, `<footer>`) y una jerarquía de encabezados lógica y sin saltos.
* **Perceptibilidad Visual:** Ajustes de contraste de color (ratio > 4.5:1) y creación de un estado de selección nítido para navegación sin ratón mediante reglas `:focus-visible`.

## 🛠️ Tecnologías Utilizadas
* HTML5 Semántico
* CSS3
* JavaScript Vanilla (Manipulación dinámica del DOM)

## ⚙️ Cómo ejecutar el proyecto

Para que las tecnologías asistivas (como NVDA o Narrador) y las herramientas de auditoría (como Lighthouse) procesen correctamente el ciclo de vida de esta SPA, es obligatorio ejecutar el proyecto bajo un servidor local:

1. Clona o descarga este repositorio en tu equipo.
2. Abre la carpeta en Visual Studio Code.
3. Instala y utiliza la extensión **Live Server** para levantar el archivo `index.html` (Puerto 5500).

## 📄 Memoria del Proyecto

Para consultar en detalle la auditoría manual, los fallos detectados inicialmente, la metodología de refactorización mediante IA y los criterios de éxito WCAG alcanzados, revisa la memoria técnica adjunta en este repositorio: **Trabajo_Accesibilidad.pdf**.
