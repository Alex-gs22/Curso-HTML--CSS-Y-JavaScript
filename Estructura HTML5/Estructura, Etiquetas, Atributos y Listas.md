# Estructura Básica en HTML

## ¿Qué es la estructura básica en HTML?

La estructura básica de un documento HTML define cómo se organiza el contenido de una página web. Incluye elementos clave que permiten a los navegadores interpretar correctamente la información.

---

## Estructura de un Documento HTML

Un documento HTML típico incluye los siguientes elementos:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Título de la Página</title>
</head>
<body>
  <h1>Encabezado Principal</h1>
  <p>Este es un párrafo de ejemplo.</p>
</body>
</html>
```

Desglose de los Elementos:

`<!DOCTYPE html>`:
Declara que el documento utiliza HTML5.

`<html>`:
Elemento raíz que contiene todo el contenido de la página. El atributo **lang="es"** indica el idioma del contenido.

`<head>`:
Contiene metadatos sobre la página (Tales como el título y enlaces a estilos o scripts).

`<meta charset="UTF-8">`:
Define la codificación de caracteres como UTF-8 para admitir caracteres especiales. Ya que por si solo los navegadores no estan configurados para admitirlos.

`<title>`:
Define el título de la página que aparece en la pestaña superior del navegador.

`<body>`:
Contiene el contenido visible de la página web.

## Etiquetas Básicas y su Función
Encabezados (`<h1>` a `<h6>`)
```html
<h1>Título Principal</h1>
<h2>Subtítulo</h2>
<h3>Tercer Nivel</h3>
<h4>Cuarto Nivel</h4>
<h5>Quinto Nivel</h5>
<h6>Sexto Nivel</h6>
```

Los encabezados estructuran jerárquicamente el contenido.
`<h1>` es el nivel más importante y `<h6>` el menos importante.

## Párrafos (`<p>`)

```html
<p>Este es un párrafo de texto que puede contener información, enlaces, y otros elementos.</p>
```

Se utiliza para agrupar texto en bloques separados.

## Enlaces (`<a>`)

```html
<a href="https://example.com" target="_blank">Visita nuestro sitio</a>
```

Crea hipervínculos para navegar a otras páginas o secciones.

## Atributos comunes

- **href**: URL del enlace.
- **target="_blank"**: Abre el enlace en una nueva pestaña.

## Atributos en las Etiquetas HTML
Los atributos son propiedades adicionales que personalizan el comportamiento o el estilo de las etiquetas HTML.

### Atributos Comunes

- **id**: Identificador único del elemento.

```html
<h1 id="titulo-principal">Título Principal</h1>
```

- **class**: Clase que permite aplicar estilos o agrupar elementos.

```html
<p class="texto-introduccion">Este es un párrafo con estilo.</p>
```

- **style**: Define estilos en línea.

```html
<p style="color: blue; font-size: 16px;">Texto azul con estilo en línea.</p>
```

- **title**: Muestra un texto emergente al pasar el cursor.

```html
<a href="https://example.com" title="Ir a Example">Enlace</a>
```

- **lang**: Especifica el idioma del contenido.

```html
<html lang="es">
```

- **data-***: Define atributos personalizados para almacenar datos.

```html
<div data-user="12345">Usuario</div>
```


## Listas en HTML
Las listas se utilizan para mostrar elementos relacionados de forma ordenada o desordenada.

### Listas Desordenadas (`<ul>`)

```html
<ul>
  <li>Elemento 1</li>
  <li>Elemento 2</li>
  <li>Elemento 3</li>
</ul>
```

Se utiliza <ul> para listas donde el orden no importa.

<li> representa cada elemento de la lista.

### Listas Ordenadas (`<ol>`)

```html
<ol>
  <li>Primer Elemento</li>
  <li>Segundo Elemento</li>
  <li>Tercer Elemento</li>
</ol>
```

Se utiliza `<ol>` para listas con un orden lógico (numeradas).

### Listas Anidadas

```html
<ul>
  <li>Elemento 1
    <ul>
      <li>Subelemento 1</li>
      <li>Subelemento 2</li>
    </ul>
  </li>
  <li>Elemento 2</li>
</ul>
```

Las listas pueden incluir otras listas dentro de sí mismas.

## Ejemplo con Listas y Atributos

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Estructura Básica</title>
</head>
<body>
  <header>
    <h1 id="titulo-principal" class="encabezado">Bienvenidos a HTML</h1>
  </header>
  
  <main>
    <section>
      <h2>Listas en HTML</h2>
      <p>Ejemplo de lista desordenada:</p>
      <ul>
        <li>HTML</li>
        <li>CSS</li>
        <li>JavaScript</li>
      </ul>
      <p>Ejemplo de lista ordenada:</p>
      <ol>
        <li>Primero</li>
        <li>Segundo</li>
        <li>Tercero</li>
      </ol>
    </section>
  </main>
</body>
</html>
```
