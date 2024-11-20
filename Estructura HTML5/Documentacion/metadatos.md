# Metadatos en HTML5

Los metadatos son información adicional sobre un documento HTML que no se muestra directamente en la página web, pero que es utilizada por navegadores, motores de búsqueda y otras herramientas para interpretar y manejar el contenido.

---

## Metadatos en HTML5 y su propósito:

### **1. Declaración de Codificación (`<meta charset>`)**

Define el conjunto de caracteres utilizado en el documento. Generalmente se utiliza `UTF-8` para soportar caracteres internacionales.

**Ejemplo:**

```html
<meta charset="UTF-8">
```

### **2. Configuración del Viewport (`<meta name="viewport">`)**

Controla cómo se muestra la página en diferentes dispositivos y tamaños de pantalla. Es fundamental para el diseño responsivo.

**Ejemplo:**

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### **3. Descripción (`<meta name="description">`)**

Proporciona un resumen del contenido de la página. Es importante para el SEO (Search Engine Optimization), ya que aparece en los resultados de búsqueda.

**Ejemplo:**

```html
<meta name="description" content="Este es un ejemplo de metadatos en HTML5">
```

### **4. Palabras Clave (`<meta name="keywords">`)**

Especifica palabras clave relacionadas con el contenido de la página. Aunque su relevancia para el SEO ha disminuido, aún puede ser útil.

**Ejemplo:**

```html
<meta name="keywords" content="HTML5, metadatos, ejemplo">
```

### **5. Autor (`<meta name="author">`)**

Indica el autor del documento.

**Ejemplo:**

```html
<meta name="author" content="Tu Nombre">
```

### **6. Robots (`<meta name="robots">`)**

Indica a los motores de búsqueda cómo indexar la página. Los valores comunes son:

  - `index`: Permite la indexación.
  - `noindex`: Evita que la página sea indexada.
  - `follow`: Permite que los enlaces sean seguidos.
  - `nofollow`: Evita que los enlaces sean seguidos.

**Ejemplo:**

```html
<meta name="robots" content="index, follow">
```

### **7. Idioma (`<meta name="language">`)**

Indica el idioma principal del documento.

**Ejemplo:**

```html
<meta name="language" content="es">
```

---

## Ejemplo Completo de Metadatos

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Este es un ejemplo de metadatos en HTML5">
    <meta name="keywords" content="HTML5, metadatos, ejemplo">
    <meta name="author" content="Tu Nombre">
    <meta name="robots" content="index, follow">
    <meta name="language" content="es">
    <title>Ejemplo de Metadatos</title>
</head>
<body>
    <h1>Ejemplo de Metadatos en HTML5</h1>
    <p>Este documento contiene ejemplos de metadatos en HTML5.</p>
</body>
</html>
```

---
