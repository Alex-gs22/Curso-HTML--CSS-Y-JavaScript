# Introducción a HTML, CSS y JavaScript

## Índice

1. [Introducción a los fundamentos de HTML, CSS y JavaScript](#introducción-a-los-fundamentos-de-html-css-y-javascript)
2. [¿Qué es HTML?](#qué-es-html)
   - [Estructura Básica](#estructura-básica)
   - [Etiquetas Comunes](#etiquetas-comunes)
   - [Atributos Comunes](#atributos-comunes)
   - [Enlaces y Navegación](#enlaces-y-navegación)
   - [Imágenes y Multimedia](#imágenes-y-multimedia)
   - [Formularios](#formularios)
3. [¿Qué es CSS?](#qué-es-css)
   - [Selectores](#selectores)
   - [Propiedades Básicas](#propiedades-básicas)
   - [Colores y Fondos](#colores-y-fondos)
   - [Posicionamiento](#posicionamiento)
   - [Flexbox y Grid](#flexbox-y-grid)
   - [Diseño Responsivo](#diseño-responsivo)
4. [¿Qué es JavaScript?](#qué-es-javascript)
   - [Variables y Tipos de Datos](#variables-y-tipos-de-datos)
   - [Funciones](#funciones)
   - [Condicionales](#condicionales)
   - [Bucles](#bucles)
   - [Funciones Flecha](#funciones-flecha)
   - [Eventos del DOM](#eventos-del-dom)
   - [Manipulación del DOM](#manipulación-del-dom)

---

## Introducción a los fundamentos de HTML, CSS y JavaScript

En esta sesión aprenderás los fundamentos de HTML, CSS y JavaScript, los tres pilares del desarrollo web. Comenzaremos con una introducción a cada tecnología, exploraremos ejemplos prácticos y finalizaremos con la creación de una página web basada en un diseño predefinido.

---

## ¿Qué es HTML?

HTML (HyperText Markup Language) es el lenguaje estándar para estructurar y diseñar contenido en la web. Define la estructura de las páginas web mediante etiquetas.

### Estructura Básica

Un documento HTML típico incluye lo siguiente:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mi Primera Página Web</title>
</head>
<body>
  <h1>Hola Mundo</h1>
  <p>¡Bienvenido a tu primera página web!</p>
</body>
</html>
```

### Etiquetas Comunes

-Algunas de las etiquetas más utilizadas son:

```html
   -<!DOCTYPE>: Define el tipo de documento.
   -<html>: Contenedor principal.
   -<head>: Contiene metadatos (como título y enlaces).
   -<body>: Contenido visible.
   -<h1> a <h6>: Encabezados.
   -<p>: Párrafos.
   -<a>: Enlaces.
   -<img>: Imágenes.
   -<ul> y <ol>: Listas desordenadas y ordenadas.
   -<li>: Elemento dentro de la lista
```
### Atributos Comunes

Explica los atributos comunes como id, class, style, y alt.

```html
<img src="imagen.jpg" alt="Descripción de la imagen" id="imagen-principal" class="responsive">
```

### Enlaces y Navegación

Cómo crear enlaces usando <a> y construir menús de navegación básicos.

```html
<nav>
  <ul>
    <li><a href="#inicio">Inicio</a></li>
    <li><a href="#servicios">Servicios</a></li>
    <li><a href="#contacto">Contacto</a></li>
  </ul>
</nav>
```

### Imágenes y Multimedia

Introducir etiquetas como <img>, <video> y <audio> para contenido multimedia.

```html
<img src="imagen.jpg" alt="Una imagen">
<video controls>
  <source src="video.mp4" type="video/mp4">
</video>
```

### Formularios

Explica cómo crear formularios básicos con etiquetas como `<input>`, `<textarea>`, `<select>` y botones.

```html
<form action="/submit" method="POST">
  <label for="nombre">Nombre:</label>
  <input type="text" id="nombre" name="nombre">
  <button type="submit">Enviar</button>
</form>
```

---

## ¿Qué es CSS?

-CSS (Cascading Style Sheets) es un lenguaje para diseñar y presentar el contenido de una página web. Define estilos como colores, fuentes y distribuciones.

### Selectores

Los selectores permiten apuntar a elementos HTML para aplicarles estilos.
```css
/* Selector por etiqueta */
h1 {
  color: blue;
}

/* Selector por clase */
.introduccion {
  font-size: 18px;
}

/* Selector por id */
#principal {
  background-color: lightgray;
}
```

### Propiedades Básicas

-color: Cambia el color del texto.
-background-color: Cambia el fondo.
-font-size: Tamaño de la fuente.
-margin y padding: Espaciado externo e interno.
-border: Define bordes.

```css
body {
  font-family: Arial, sans-serif;
  background-color: #f4f4f4;
  color: #333;
}
```

### Colores y Fondos

Diferentes maneras de usar colores (hex, rgb, hsl) y aplicar fondos con background.

```css
body {
  color: #333;
  background: linear-gradient(to right, #4caf50, #2196f3);
}
```

### Posicionamiento

Explica cómo funciona el modelo de caja y cómo usar propiedades como position, z-index, y float.

```css
.caja {
  position: absolute;
  top: 50px;
  left: 100px;
}
```

### Flexbox y Grid

Introduce conceptos modernos de diseño como display: flex; y display: grid;.

```css
.contenedor {
  display: flex;
  justify-content: center;
  align-items: center;
}

.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
}
```

### Diseño Responsivo

El diseño responsivo adapta la apariencia de la página a diferentes tamaños de pantalla. Utilizamos media queries para lograrlo.

```css
@media (max-width: 768px) {
  body {
    font-size: 14px;
  }
}
```

---

## ¿Qué es JavaScript?

JavaScript es un lenguaje de programación que permite agregar interactividad y funcionalidad a las páginas web.

### Variables y Tipos de Datos

```javascript
// Declaración de variables
let nombre = "Juan";
const edad = 25;

// Tipos de datos
let numero = 42; // Número
let texto = "Hola"; // Cadena
let booleano = true; // Booleano
let arreglo = [1, 2, 3]; // Arreglo
let objeto = { clave: "valor" }; // Objeto
```

### Funciones

Las funciones permiten reutilizar bloques de código.

```javascript
function saludar(nombre) {
  return `Hola, ${nombre}!`;
}

console.log(saludar("Juan"));
```

### Condicionales

Introduce estructuras como if, else, y switch para tomar decisiones.

```javascript
let edad = 18;

if (edad >= 18) {
  console.log("Eres mayor de edad");
} else {
  console.log("Eres menor de edad");
}
```

### Bucles

Explica cómo usar for, while, y forEach para repetir tareas.

```javascript
for (let i = 0; i < 5; i++) {
  console.log("Iteración: " + i);
}
```

### Funciones Flecha

Introducir la sintaxis moderna para funciones.

```javascript
const saludar = (nombre) => `Hola, ${nombre}!`;
console.log(saludar("Juan"));
```

### Eventos del DOM

Cómo responder a eventos como click o mouseover.
```javascript
document.querySelector("button").addEventListener("click", () => {
  alert("¡Hiciste clic!");
});
```

### Manipulación del DOM

El DOM (Document Object Model) permite interactuar con elementos HTML.

```javascript
// Seleccionar un elemento
let titulo = document.querySelector("h1");

// Cambiar el contenido
titulo.textContent = "Nuevo Título";

// Agregar un evento
titulo.addEventListener("click", function () {
  alert("¡Hiciste clic en el título!");
});
```
