
# Hojas de Estilo en Cascada (CSS)

CSS (Cascading Style Sheets) es un lenguaje utilizado para describir la presentación y diseño de un documento HTML. Permite separar la estructura (HTML) del estilo (CSS), haciendo el código más limpio y modular.

---

## 1. **Definición**

CSS se utiliza para definir estilos visuales como colores, fuentes, tamaños y distribuciones. Se aplica a elementos HTML utilizando selectores y propiedades específicas, permitiendo un control preciso sobre el diseño de las páginas web.

**Ventajas de CSS:**
- Facilita el mantenimiento del código al separar el diseño de la estructura.
- Permite aplicar estilos consistentes en múltiples páginas.
- Mejora la experiencia del usuario mediante diseños responsivos.

---

## 2. **Selectores en CSS**

Los selectores son patrones utilizados para apuntar a elementos HTML y aplicarles estilos.

### **Tipos de Selectores**

1. **Universal (`*`)**
   Selecciona todos los elementos de la página.
   ```css
   * {
     margin: 0;
     padding: 0;
   }


2. **De Tipo**
   Selecciona todos los elementos de un tipo específico.
   ```css
   p {
     color: blue;
   }
   ```

3. **Clases (`.`)**
   Selecciona elementos con una clase específica. Se usa el prefijo `.`.
   ```css
   .destacado {
     font-weight: bold;
   }
   ```

4. **ID (`#`)**
   Selecciona un elemento único identificado por un ID. Se usa el prefijo `#`.
   ```css
   #titulo {
     text-align: center;
   }
   ```

5. **Por Atributo**
   Selecciona elementos con atributos específicos.
   ```css
   input[type="text"] {
     border: 1px solid black;
   }
   ```

6. **Descendiente**
   Selecciona elementos dentro de otros elementos.
   ```css
   div p {
     color: gray;
   }
   ```

7. **Pseudoclases**
   Selecciona elementos basados en su estado o posición.
   ```css
   a:hover {
     color: red;
   }
   ```

---

## 3. **Ejemplo Práctico**

### **Archivo `index.html`**
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ejemplo de Selectores CSS</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1 id="titulo">Bienvenido a CSS</h1>
  <p class="destacado">Este párrafo es destacado mediante una clase.</p>
  <p>Este párrafo tiene estilos básicos.</p>
  <div>
    <p>Este es un párrafo dentro de un contenedor.</p>
  </div>
  <input type="text" placeholder="Texto de ejemplo">
  <a href="#">Enlace de ejemplo</a>
</body>
</html>
```

---

### **Archivo `style.css`**
```css
/* Universal */
* {
  margin: 0;
  padding: 0;
}

/* De Tipo */
p {
  font-size: 16px;
  color: black;
}

/* Clase */
.destacado {
  font-weight: bold;
  color: blue;
}

/* ID */
#titulo {
  text-align: center;
  font-size: 24px;
  color: darkgreen;
}

/* Por Atributo */
input[type="text"] {
  border: 2px solid gray;
  padding: 5px;
}

/* Descendiente */
div p {
  color: gray;
  font-style: italic;
}

/* Pseudoclases */
a:hover {
  color: red;
  text-decoration: underline;
}
```

---

## 4. **Tipos de Selectores**

| **Tipo de Selector** | **Sintaxis**      | **Descripción**                                                       |
|-----------------------|-------------------|------------------------------------------------------------------------|
| Universal            | `*`              | Aplica estilos a todos los elementos del documento.                   |
| De Tipo              | `p`, `h1`, etc.  | Selecciona elementos de un tipo específico.                           |
| Clase                | `.clase`         | Selecciona elementos con una clase específica.                        |
| ID                   | `#id`            | Selecciona un único elemento con un ID específico.                    |
| Por Atributo         | `[atributo]`     | Selecciona elementos que tienen un atributo específico.               |
| Descendiente         | `padre hijo`     | Selecciona elementos hijo dentro de un elemento padre.                |
| Pseudoclases         | `selector:pseudo`| Selecciona elementos en un estado o posición específica (por ejemplo, `:hover`). |

---

# Especificidad en CSS

La especificidad es un sistema que CSS utiliza para determinar qué reglas de estilo se aplican a un elemento cuando existen múltiples reglas en conflicto. Es crucial para entender cómo funciona el orden de prioridad en las Hojas de Estilo en Cascada.

---

## **1. ¿Qué es la especificidad?**

La especificidad es una medida de qué tan específico es un selector. Cuanto más específico sea, mayor prioridad tendrá en comparación con reglas más generales.

CSS asigna un "peso" a cada selector basado en el tipo de selector que utiliza. Estos pesos se comparan para determinar qué estilos se aplican al elemento.

---

## **2. Cómo funcionan las Hojas de Estilo en Cascada**

CSS utiliza un modelo en cascada para aplicar estilos, en el que las reglas se procesan en el siguiente orden de prioridad:

1. **Reglas con `!important`:**
   Sobrescriben cualquier otra regla, independientemente de su especificidad.

2. **Estilos en línea (`style="..."`):**
   Tienen prioridad sobre cualquier regla en hojas de estilo externas o internas.

3. **Especificidad de selectores:**
   Los selectores más específicos tienen prioridad sobre los más generales. El orden jerárquico es:
   - Identificadores (`#id`)
   - Clases (`.clase`), pseudoclases (`:hover`, `:first-child`) y atributos (`[atributo]`)
   - Elementos (`h1`, `p`, etc.) y pseudoelementos (`::before`, `::after`)

4. **Orden de las reglas:**
   Si dos reglas tienen la misma especificidad, la última regla definida en el código será la que se aplique.

---

## **3. Tabla de Especificidad y Prioridad**

| **Selector**                  | **Especificidad**     | **Ejemplo**            |
|-------------------------------|-----------------------|-------------------------|
| Estilos en línea              | Máxima               | `<p style="color: red;">Texto</p>` |
| `!important`                  | Alta (sobrescribe todo) | `color: blue !important;` |
| Identificadores (`#id`)       | 100                  | `#titulo { color: red; }` |
| Clases, pseudoclases y atributos | 10                 | `.clase`, `:hover`, `[type="text"]` |
| Elementos y pseudoelementos   | 1                    | `p`, `::before`, `h1`   |

---

## **4. Ejemplo Práctico**

### **Archivo `index.html`**
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ejemplo de Especificidad</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1 id="titulo" class="encabezado">Encabezado Principal</h1>
  <p class="texto">Texto general con estilos por clase.</p>
  <p class="texto" style="color: green;">Texto con estilos en línea.</p>
</body>
</html>
```

---

### **Archivo `style.css`**
```css
/* Estilos básicos */
h1 {
  color: blue; /* Prioridad más baja */
}

/* Estilo por clase */
.encabezado {
  color: orange; /* Sobrescribe el estilo de `h1` */
}

/* Estilo por ID */
#titulo {
  color: red; /* Sobrescribe clase y etiqueta */
}

/* Estilo en línea */
p[style] {
  color: green; /* Sobrescribe las reglas de las clases y etiquetas */
}

/* !important */
p.texto {
  color: purple !important; /* Sobrescribe incluso el estilo en línea */
}
```

---

## **5. Resultado del Ejemplo**

1. El `<h1>` mostrará texto en **rojo**, porque el estilo del ID (`#titulo`) tiene mayor especificidad que el de clase o etiqueta.
2. El primer `<p>` con clase `texto` usará el estilo **morado** debido al uso de `!important`.
3. El segundo `<p>` mostrará texto en **verde**, porque el estilo en línea tiene mayor prioridad.

---

## **6. Reglas de Cascada: Orden de Importancia**

| **Nivel de Prioridad** | **Regla**                      | **Ejemplo**                          |
|-------------------------|--------------------------------|--------------------------------------|
| 1 (Máxima)             | `!important`                  | `color: blue !important;`           |
| 2                      | Estilos en línea              | `<p style="color: red;">Texto</p>`  |
| 3                      | Identificadores (`#id`)       | `#titulo { color: red; }`           |
| 4                      | Clases, pseudoclases, atributos | `.clase`, `:hover`, `[type="text"]` |
| 5 (Mínima)             | Elementos y pseudoelementos   | `p`, `::before`, `h1`               |

---
