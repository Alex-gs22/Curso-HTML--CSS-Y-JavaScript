# **Propiedades de las Cajas en CSS**

En CSS, las cajas representan la estructura y diseño de los elementos HTML. Estas cajas tienen propiedades que definen su tamaño, apariencia, espaciado interno y externo, bordes y más.

---

## **1. Tamaño de las Cajas**

El tamaño de una caja está determinado por las propiedades `width` y `height`.

```css
.caja {
  width: 200px; /* Ancho */
  height: 100px; /* Alto */
}
```

---

## **2. Color de Fondo**

Define el color o imagen que llena el fondo de la caja.

### **Color de Fondo (`background-color`):**

```css
.caja {
  background-color: lightblue; /* Fondo azul claro */
}
```

### **Imagen de Fondo (`background-image`):**

```css
.caja {
  background-image: url('imagen.jpg'); /* Imagen como fondo */
  background-size: cover; /* Ajusta la imagen al tamaño de la caja */
}
```

---

## **3. Letra**

Controla el texto dentro de la caja.

```css
.caja {
  font-size: 16px; /* Tamaño de la fuente */
  font-family: Arial, sans-serif; /* Familia de fuentes */
  color: black; /* Color del texto */
}
```

---

## **4. Bordes (`border`)**

Define el contorno de la caja.

```css
.caja {
  border: 2px solid black; /* Borde sólido negro de 2px */
}
```

---

## **5. Esquinas Redondeadas (`border-radius`)**

Permite redondear las esquinas de la caja.

```css
.caja {
  border-radius: 10px; /* Esquinas redondeadas */
}
```

---

## **6. Espaciado Interno (`padding`)**

El espacio entre el contenido de la caja y su borde.

```css
.caja {
  padding: 20px; /* Espaciado interno de 20px */
}
```

### Representación Visual del Padding:
(Espacio para la imagen que muestra las diferentes áreas del padding alrededor del contenido).

---

## **7. Espaciado Externo (`margin`)**

El espacio entre la caja y otros elementos cercanos.

```css
.caja {
  margin: 20px; /* Espaciado externo de 20px */
}
```

### Representación Visual del Margin:
(Espacio para la imagen que muestra las áreas de margen alrededor de la caja).

---

## **8. Sombra de la Caja (`box-shadow`)**

Añade sombras a la caja.

```css
.caja {
  box-shadow: 4px 4px 10px rgba(0, 0, 0, 0.5); /* Sombra negra con transparencia */
}
```

---

## **Ejemplo Completo**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Propiedades de las Cajas</title>
  <style>
    .caja {
      width: 300px;
      height: 150px;
      background-color: lightblue;
      border: 3px solid black;
      border-radius: 10px;
      padding: 20px;
      margin: 30px;
      box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.4);
      font-size: 16px;
      font-family: Arial, sans-serif;
      color: black;
    }
  </style>
</head>
<body>
  <div class="caja">Esta es una caja con múltiples propiedades aplicadas.</div>
</body>
</html>
```

---

## **Tabla de Propiedades de las Cajas**

| **Propiedad**       | **Descripción**                                                       |
|---------------------|-----------------------------------------------------------------------|
| `width`, `height`   | Define el ancho y alto de la caja.                                   |
| `background-color`  | Establece el color de fondo.                                         |
| `background-image`  | Establece una imagen como fondo.                                     |
| `font-size`         | Tamaño del texto dentro de la caja.                                  |
| `font-family`       | Define la familia tipográfica.                                       |
| `border`            | Establece el estilo, ancho y color del borde.                       |
| `border-radius`     | Permite redondear las esquinas de la caja.                          |
| `padding`           | Espaciado interno entre el contenido y el borde.                    |
| `margin`            | Espaciado externo entre la caja y otros elementos.                  |
| `box-shadow`        | Añade sombra a la caja para resaltar su apariencia.                 |

---

### 🌐 Navegación

- <-- Anterior : [Teoría de Cajas](Teoría%20de%20Cajas.md)
- --> Siguiente : [](.md)

  
