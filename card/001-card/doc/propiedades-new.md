
# transform-style: preserve-3d
La propiedad transform-style: preserve-3d es una propiedad CSS que establece cómo los elementos hijos anidados son renderizados en el espacio 3D.

- Cuando se establece en preserve-3d:
Permite que los elementos hijos mantengan su posición en el espacio tridimensional

- Es esencial para crear efectos 3D cuando se usan transformaciones como rotate, translate3d, o perspective.

- Los elementos hijos se renderizarán en su propio plano 3D en lugar de ser aplanados en el plano del elemento padre

En este código específico, se está aplicando a un elemento figure, probablemente como parte de una tarjeta que tendrá algún efecto de volteo o rotación 3D, ya que también tiene una propiedad transition definida.

Sin preserve-3d, cualquier transformación 3D aplicada a los elementos hijos se "aplastaría" en un plano 2D, perdiendo el efecto de profundidad deseado.

- Esta propiedad es comúnmente utilizada en:
- Efectos de volteo de tarjetas
- Cubos 3D
- Carruseles con efecto 3D
- Cualquier animación que requiera mantener la perspectiva tridimensional

# backface-visibility: hidden;
La propiedad backface-visibility en CSS determina si la cara posterior de un elemento debe ser visible cuando se gira hacia el usuario.

En el contexto de tu código, donde se usa para una tarjeta con efecto de volteo, aquí está la explicación:

```css
figure .frontal {
    display: block;
    backface-visibility: hidden;
}
```
Los valores posibles son:
- __hidden:__ Oculta la cara posterior del elemento.
- __visible:__ (valor por defecto) Muestra la cara posterior del elemento.

Cuando se establece como hidden:

1. Cuando el elemento se gira (por ejemplo, con transform: rotateY(180deg)), la cara posterior será invisible.

2. Esto es especialmente útil en efectos de tarjetas 3D donde no quieres ver el reverso del elemento frontal cuando la tarjeta se voltea.

3. Ayuda a crear una ilusión más limpia en animaciones de volteo.

En tu código específico, **backface-visibility: hidden** se aplica al lado frontal de la tarjeta para que cuando se gire, no se vea su parte posterior, creando así un efecto más realista de una tarjeta que se voltea.

Este efecto es comúnmente usado junto con:

- transform-style: preserve-3d
- Transformaciones 3D
- Transiciones