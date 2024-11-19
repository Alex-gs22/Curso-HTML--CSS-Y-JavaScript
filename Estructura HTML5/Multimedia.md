# Multimedia en HTML

HTML permite integrar diversos tipos de contenido multimedia, como imágenes, videos y audio, para enriquecer la experiencia de los usuarios.

---

## 1. **Imágenes (`<img>`)**

La etiqueta `<img>` se utiliza para insertar imágenes en una página web.

### Sintaxis Básica

```html
<img src="ruta/imagen.jpg" alt="Descripción de la imagen" width="300">
```

---

## 2. **Videos (`<video>`)**

La etiqueta `<video>` permite reproducir videos directamente en la página.

### Sintaxis Básica

```html
<video controls width="600">
  <source src="ruta/video.mp4" type="video/mp4">
</video>
```

---

## 3. **Audio (`<audio>`)**

La etiqueta <audio> permite reproducir archivos de audio.

### Sintaxis Básica

```html
<audio controls>
  <source src="ruta/audio.mp3" type="audio/mpeg">
</audio>
```

---


## 4. **Atributos Comunes en `Multimedia`**


### `src`: Especifica la ubicación de la imagen (ruta relativa o absoluta).

### `alt`: Proporciona un texto alternativo que describe la imagen (importante para accesibilidad y SEO).

### `width` y `height`: Controlan las dimensiones de la imagen.


```html
<img src="logo.png" alt="Logotipo de la empresa" width="200">
```

### `controls`

Agrega controles para que el usuario pueda reproducir, pausar, ajustar el volumen o avanzar en la reproducción.

```html
<video controls width="600">
  <source src="video.mp4" type="video/mp4">
</video>
```

Este video mostrará un conjunto de controles (play, pausa, volumen, barra de progreso) que el usuario podrá manipular.

### `autoplay`

Reproduce automáticamente el contenido en cuanto la página se carga. Requiere el atributo muted para funcionar en la mayoría de los navegadores modernos (para evitar reproducción automática con sonido).

```html
<video autoplay muted width="600">
  <source src="video.mp4" type="video/mp4">
</video>
```

El video comenzará a reproducirse automáticamente sin sonido al cargar la página.

### `loop`

Reproduce el contenido en un bucle continuo, reiniciándose automáticamente al llegar al final.

```html
<audio loop>
  <source src="audio.mp3" type="audio/mpeg">
</audio>
```

El archivo de audio se reproducirá continuamente, reiniciándose automáticamente al terminar.

### `muted`

El contenido se reproduce con el audio silenciado.

```html
<video controls muted width="600">
  <source src="video.mp4" type="video/mp4">
</video>
```

El video tendrá sonido silenciado por defecto, aunque el usuario podrá activarlo manualmente desde los controles.

### `poster`

Especifica una imagen que se mostrará como vista previa antes de reproducir el video.

```html
<video controls poster="preview.jpg" width="600">
  <source src="video.mp4" type="video/mp4">
</video>
```

El video mostrará la imagen preview.jpg como portada mientras está detenido o antes de que el usuario lo inicie.

---

## Comparación de Atributos entre `<video>`, `<audio>` y `<img>`

| **Atributo**  | **Descripción**                                                                 | **Disponible en `<video>`** | **Disponible en `<audio>`** | **Disponible en `<img>`** |
|----------------|---------------------------------------------------------------------------------|-----------------------------|-----------------------------|---------------------------|
| `src`         | Ubicación del archivo multimedia. Especifica la ruta del recurso.               | Sí                          | Sí                          | Sí                        |
| `alt`         | Texto alternativo que describe el contenido (accesibilidad).                    | No                          | No                          | Sí                        |
| `width`       | Define el ancho del reproductor o de la imagen (en píxeles).                    | Sí                          | No                          | Sí                        |
| `height`      | Define el alto del reproductor o de la imagen (en píxeles).                     | Sí                          | No                          | Sí                        |
| `controls`    | Agrega controles para reproducir, pausar o ajustar el volumen.                  | Sí                          | Sí                          | No                        |
| `autoplay`    | Reproduce automáticamente el contenido al cargar la página.                     | Sí                          | Sí                          | No                        |
| `loop`        | Reproduce el contenido en bucle continuo.                                       | Sí                          | Sí                          | No                        |
| `muted`       | Reproduce el contenido con el audio silenciado por defecto.                     | Sí                          | Sí                          | No                        |
| `poster`      | Imagen que se muestra como vista previa antes de reproducir el contenido.       | Sí                          | No                          | No                        |

---

