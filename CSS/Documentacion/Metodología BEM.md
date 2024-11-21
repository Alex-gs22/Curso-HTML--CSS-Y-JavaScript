# Metodología BEM (Block, Element, Modifier)

BEM (Block, Element, Modifier) es una metodología de desarrollo de CSS diseñada para mantener el código organizado, modular y escalable. Fue introducida por el equipo de desarrollo de Yandex para resolver problemas relacionados con la reutilización de estilos y la mantenibilidad en proyectos complejos.

---

## **1. Definición**

BEM divide los componentes de una interfaz en tres partes principales:

- **Block (Bloque):** Representa un componente independiente, como un botón, una tarjeta o un formulario.
- **Element (Elemento):** Es una parte de un bloque, como el texto dentro de un botón o una etiqueta en un formulario.
- **Modifier (Modificador):** Representa una variación o estado del bloque o elemento, como un botón deshabilitado o un tema oscuro.

---

## **2. Sintaxis**

La nomenclatura BEM sigue este formato:

```css
.block {}
.block__element {}
.block--modifier {}
```

- **Bloques (`.block`)**: Identifican un componente único.
- **Elementos (`.block__element`)**: Representan partes específicas de un bloque, unidos al bloque con dos guiones bajos (`__`).
- **Modificadores (`.block--modifier`)**: Representan variaciones o estados, unidos al bloque o elemento con dos guiones (`--`).

---

## **3. Ejemplo Práctico**

### **HTML**
```html
<div class="card card--featured">
  <h2 class="card__title">Título de la Tarjeta</h2>
  <p class="card__description">Descripción de la tarjeta.</p>
  <button class="card__button card__button--primary">Leer más</button>
</div>
```

### **CSS**
```css
/* Bloque */
.card {
  border: 1px solid #ccc;
  padding: 16px;
  border-radius: 8px;
}

/* Elementos */
.card__title {
  font-size: 1.5rem;
  color: #333;
}

.card__description {
  font-size: 1rem;
  color: #666;
}

.card__button {
  padding: 8px 16px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

/* Modificadores */
.card--featured {
  background-color: #f9f9f9;
  border-color: #007bff;
}

.card__button--primary {
  background-color: #0056b3;
}

.card__button--disabled {
  background-color: #ccc;
  cursor: not-allowed;
}
```

---

## **4. Beneficios de BEM**

1. **Modularidad:** Cada bloque es independiente, lo que facilita su reutilización en diferentes partes del proyecto.
2. **Escalabilidad:** Facilita la gestión de proyectos grandes al mantener un código CSS bien estructurado.
3. **Evita conflictos de estilos:** Al usar una nomenclatura única, es menos probable que los estilos se sobreescriban accidentalmente.
4. **Mantenibilidad:** Es fácil identificar a qué parte del HTML pertenece un estilo en el CSS.

---

## **5. Buenas Prácticas en BEM**

- **Usar nombres descriptivos:** Los nombres de bloques, elementos y modificadores deben ser claros y representar su propósito.
- **Evitar anidaciones profundas:** Mantén los selectores planos y directos.
- **Reutilizar bloques y elementos:** Si un componente ya existe, reutilízalo en lugar de crear uno nuevo.

---

## **6. Comparación: CSS Convencional vs BEM**

### **CSS Convencional**
```html
<div class="card">
  <h2 class="title">Título</h2>
  <button class="btn primary">Botón</button>
</div>
```

```css
.card {
  border: 1px solid #ccc;
}

.title {
  font-size: 1.5rem;
}

.btn.primary {
  background-color: #007bff;
}
```

Problemas:
- Las clases `.title` y `.btn.primary` pueden entrar en conflicto si se reutilizan en otros contextos.

### **BEM**
```html
<div class="card card--featured">
  <h2 class="card__title">Título</h2>
  <button class="card__button card__button--primary">Botón</button>
</div>
```

```css
.card {
  border: 1px solid #ccc;
}

.card__title {
  font-size: 1.5rem;
}

.card__button--primary {
  background-color: #007bff;
}
```

Ventajas:
- Cada clase está claramente vinculada a su bloque, evitando conflictos.

---
