# Introducción a la Semántica en HTML

## ¿Qué es la semántica en HTML?

La semántica en HTML se refiere al uso correcto de etiquetas para describir el propósito y significado del contenido dentro de una página web. Esto permite que el navegador, los motores de búsqueda y los lectores de pantalla interpreten el contenido de manera más precisa.

---

## ¿Por qué es importante la semántica?

1. **Accesibilidad:**
   - Facilita que tecnologías asistivas (como lectores de pantalla) identifiquen partes clave del sitio.
   - Mejora la experiencia para usuarios con discapacidades.

2. **Optimización SEO:**
   - Los motores de búsqueda como Google entienden mejor la estructura del contenido, mejorando la visibilidad en resultados.

3. **Claridad en el código:**
   - Hace que el código sea más fácil de leer y mantener para desarrolladores.

4. **Cumplimiento de estándares web:**
   - Usar etiquetas semánticas garantiza que tu página sea más moderna y compatible con futuras tecnologías.

---

## Ejemplos de etiquetas semánticas

| **Etiqueta**    | **Propósito**                                                                 |
|------------------|-------------------------------------------------------------------------------|
| `<header>`      | Encabezado de una página o sección.                                          |
| `<nav>`         | Agrupa enlaces de navegación.                                               |
| `<main>`        | Contenido principal de la página.                                           |
| `<section>`     | Agrupa contenido relacionado dentro de una sección temática.                |
| `<article>`     | Contenido independiente y reutilizable, como un artículo de blog.           |
| `<aside>`       | Contenido relacionado o secundario, como barras laterales.                  |
| `<footer>`      | Pie de página de una sección o página completa.                             |
| `<figure>`      | Contiene imágenes, gráficos o tablas junto con una descripción.             |
| `<figcaption>`  | Proporciona una descripción para el contenido de `<figure>`.                |

---

## Ejemplo Comparativo

### **HTML sin semántica:**
```html
<div>
  <div>
    <h1>Título de la Página</h1>
  </div>
  <div>
    <p>Este es un párrafo de ejemplo.</p>
  </div>
</div>
