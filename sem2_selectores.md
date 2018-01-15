# Selectores

Los selectores, como se mencionó anteriormente, indican a qué elementos HTML se le está aplicando estilo. Es importante comprender completamente cómo usar los selectores y cómo se pueden aprovechar. El primer paso es familiarizarse con los diferentes tipos de selectores. Comenzaremos con los selectores más comunes: tipo , clase y selectores de ID .

## Selectores de Tipo

Los selectores de tipo seleccionan elementos basados en su nombre. Por ejemplo, si deseamos dirigirnos a todos los elementos `<div>` usaríamos un selector de tipo de div. El siguiente código muestra un selector de tipo para los elementos de `<div>`, así como el HTML correspondiente que selecciona.

Ejemplo:

```css
div {
    background-color: #89c877;
}
```

## Selectores de clase

Los selectores de clase nos permiten seleccionar un elemento basado en el valor del atributo __class__ del elemento. Los selectores de clase son un poco más específicos que los selectores de tipo, ya que seleccionan un grupo particular de elementos en lugar de todos los elementos de un tipo.

Dentro de CSS, las clases se denotan por un punto inicial __.__, seguido del nombre de __class__ del atributo. Aquí el selector de clase seleccionará cualquier elemento que contenga el nombre de la clase del atributo __awesome__, incluidos los elementos de división y de párrafo.

Ejemplo:

```css
.awesome {
    background: red;
    margin: 12px;
    padding: 12px;
}
```

```html
<div class="awesome">...</div>
<p class="awesome">...</p>
```

## Selectores de ID

Los selectores de ID son incluso más precisos que los selectores de clase, ya que solo se dirigen a un elemento único a la vez. Así como los selectores de clase usan el valor class de atributo de un elemento como selector, los selectores de ID usan el valor __id__ de atributo de un elemento como selector.

Independientemente del tipo de elemento en el que aparezcan, los valores de __id__ de los atributos solo se pueden usar una vez por página. Si se usan, deberían reservarse para elementos significativos.

Dentro de CSS, los selectores de ID se denotan con un signo numeral __#__, seguido del valor de __id__ del atributo. Aquí el selector de ID solo seleccionará el elemento que contiene el valor id de atributo de __unico__.

```css
#unico {
    background: black;
    margin: 12px;
    padding: 12px;
}
```

```html
<div id="unico">...</div>
```

En el siguiente ejemplo veremos como se hace uso de los selectores:

Para visualizar hacer click [aquí](https://codepen.io/gersongams/pen/dJjqwo)

```html
<!DOCTYPE html>
<html lang="es">
    <head>
        <title>Hackspace</title>
        <style type="text/css">
            /* Selector de tipo */
            p {
                text-align: center;
                color: red;
            } 
            /* Selector de id */
            #para1 {
                font-size: 20px;
            }

            /* Selector de clase */

            .caja{
              background: black;
            }
        </style>
    </head>

    <body>

        <p>Cada párrafo será afectado por el selector de clase.</p>
        <p id="para1">Este párrafo tambien</p>
        <p>Y este</p>
        <div class="caja"> 
          <p> HackSpace</p>
        </div>

    </body>
</html>
```

