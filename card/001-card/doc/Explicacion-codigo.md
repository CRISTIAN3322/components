## HTML

Te explico el código HTML:

Este es un diseño de tarjetas con efecto 3D. Vamos a desglosarlo:

1. Estructura básica:

- El código comienza con la estructura HTML5 estándar

- Incluye un archivo CSS externo llamado "main.css"

- El título de la página es "Card 3D"

2. Contenido principal:

- Hay un contenedor principal con clase "contenedor"

- Dentro hay tres "contenedor_tarjeta" idénticos en estructura

3. Cada tarjeta contiene:

- Un enlace \<a>

- Un elemento \<figure> que contiene:

 -Una imagen frontal con clase "frontal"

 -Un \<figcaption> con clase "trasera" que incluye:

  - Un título \<h2>

  - Una línea horizontal \<hr>

  - Un párrafo <p> con texto

4. Las tres tarjetas son idénticas en estructura pero cada una tiene una imagen diferente:

- img-01.jpg
- img-02.jpg
- img-03.jpg

Este código está diseñado para crear tarjetas que probablemente tengan un efecto de volteo o transformación 3D cuando el usuario interactúe con ellas (esto se definirá en el archivo CSS que no está mostrado aquí).

Las tarjetas tienen una cara frontal (la imagen) y una cara trasera (con título y texto), sugiriendo que habrá algún tipo de animación o transición entre ambas caras.

## CSS

Te explico el código CSS:
1. Configuración básica:
 ```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```
Esto resetea los márgenes y rellenos predeterminados y establece el modelo de caja.

2. Contenedor principal:
```css
.contenedor {
    max-width: 1200px;
    margin: 50px auto;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
}
```
Crea un contenedor flexible que centra las tarjetas y las organiza en filas.
3. Efecto de volteo de tarjeta:
```css
.contenedor_tarjeta:hover figure {
    transform: perspective(600px) rotateY(180deg);
}
```
Cuando pasas el cursor sobre la tarjeta, esta gira 180 grados en el eje Y.
4. Estructura de la tarjeta:
- **frontal:** La parte delantera de la tarjeta con la imagen
- **trasera:** La parte posterior con información adicional
```css
figure .trasera {
    position: absolute;
    top: 0;
    padding: 20px;
    color: #fff;
    transform: perspective(600px) rotateY(180deg);
    backface-visibility: hidden;
}
```
5. Responsive:
```css
@media screen and (max-width:992px) {
    figure .trasera {
        backface-visibility: visible;
        transform: perspective(600px) rotateY(0deg);
    }
}

```
En pantallas pequeñas, desactiva el efecto de volteo y muestra el contenido posterior de manera normal.

Este código crea tarjetas interactivas que giran al pasar el cursor sobre ellas, mostrando información adicional en la parte posterior. Incluye efectos como desenfoque de imagen y sombras para mejorar la experiencia visual.

