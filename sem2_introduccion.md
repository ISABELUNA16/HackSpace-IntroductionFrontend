# Iniciando con CSS

En la primera semana vimos los aspectos básicos de la creación de paginas web con HTML, pero estas se veían un poco tristes, sin color, sin estilo. Ahora vamos a ver como hacer para que nuestras páginas se vean muy bien y sean presentables para nuestro público.

## ¿Qué es CSS? 

CSS (Cascading Style Sheets, que significa 'hojas de estilo en cascada') es un lenguaje utilizado para describir el aspecto y el formato de un sitio web escrito en lenguaje de marcado (como HTML). 

## ¿Por qué usar CSS?

CSS ayuda a mantener la información de contenido de un documento separado de los detalles de como mostrarlo. Los detalles de como se muestra el documento son conocidos como estilos. Si mantienes los estilos separados del contenido puedes:

* Evitar duplicación
* Hacer el mantenimiento más simple
* Usar el mismo contenido con diferentes estilos para diferentes propositos.

## Sintaxis de un archivo CSS

### Selectores

A medida que los elementos se agregan a una página web, se pueden agregar estilos con CSS. Un selector designa exactamente a qué elemento o elementos dentro de nuestro HTML se les debe aplicar estilos (como color, tamaño y posición). Los selectores pueden incluir una combinación de diferentes calificadores para seleccionar elementos únicos, todo dependiendo de qué tan específicos deseamos ser. Por ejemplo, podemos desear seleccionar cada párrafo en una página, o podemos desear seleccionar solamente un párrafo específico en una página.

Los selectores están generalmente dirigidos a un valor de atributo, tal como __id__, valor de __clase__, o directamente el tipo de elemento, tal como `<h1>`o `<p>`.

Dentro de CSS, los selectores se siguen con corchetes, {} que abarcan los estilos que se aplicarán al elemento seleccionado. El selector aquí apunta a todos los `<p>`elementos.

```css
/* Ejemplo de selector */
p{
    ...
}
```

### Propiedades

Una vez que se selecciona un elemento, una propiedad determina los estilos que se aplicarán a ese elemento. Los nombres de propiedades caen después de un selector, dentro de los corchetes, {} y que precede inmediatamente dos puntos __:__. Hay numerosas propiedades que podemos utilizar, como __background__, __color__, __font-size__, __height__, y __width__, y otras. 

En el siguiente código, estamos definiendo las propiedades que se le aplicaran a todos los elementos `<p>` como el color y tamaño de fuente.

```css
p {
  color: ...;
  font-size: ...;
}
```

### Valores

Hasta ahora, hemos seleccionado un elemento con un selector y hemos determinado qué estilo queremos aplicar con una propiedad. Ahora podemos determinar el comportamiento de esa propiedad con un valor. Los valores pueden ser identificados como el texto entre los dos puntos (:() y el punto y coma (;). 

En el siguiente ejemplo estamos asignando valores a nuestras propiedades de la etiqueta `<p>`.


```css
p {
  color: orange;
  font-size: 16px;
}
```

La siguiente imagen resumen lo antes descrito:

<p align="center">
<img src="https://learn.shayhowe.com/assets/images/courses/html-css/building-your-first-web-page/css-syntax-outline.png">
</p>

## ¿Cómo usamos CSS?

Ahora vamos a ver como podemos usar CSS con HTML.

Hay tres formas de insertar una hoja de estilo en nuestra página web:

* Estilo en linea
* Hoja de estilo interna
* Hoja de estilo externa

### Estilos en linea

Los estilos en una línea son declaraciones CSS que afetan solo a un elemento que está contenido dentro de un atributo style:

No usar a menos que sea necesario, ya que su mantenimiento es verdaderamente complicado (podríamos tener que actualizar la misma información muchas veces en cada documento), además de mezclar la información de estilo con la información estructural del HTML, haciendo el CSS difícil de leer y de entender. Manteniendo los distintos tipos de código separados y puros, facilitará la tarea a aquellos que vayan a trabajar posteriormente en el código.

Si deseas ver el resultado click [aquí](https://codepen.io/gersongams/pen/ypqxyo).

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Estilos</title>
    </head>

    <body style="background-color:powderblue;">

        <h1 style="color:blue;">Esto es h1 de color azul</h1>
        <p style="color:red;">Esto es un parrafo de color verde</p>

        <h1 style="font-family:verdana;">Esto es h1 de tipo Verdana</h1>
        <p style="font-family:courier;">Esto es un parrafo de tipo courier</p>

        <h1 style="font-size:300%;">Esto es h1 de tamaño 300%</h1>
        <p style="font-size:160%;">Esto es un parrafo de tamaño 160%</p>

        <h1 style="text-align:center;">Esto es h1 centrado</h1>
        <p style="text-align:right;">Esto es un parrafo alineado a la derecha</p>

        <h1 style="color:blue; font-family:verdana; font-size:300% ; text-align:center;"> Hackspace </h1>
    </body>
</html>
```

### Hoja de estilo interna

En un CSS interno ubicamos los estilos dentro de un elemento 
`<style>`, en el apartado HTML head. Así, el HTML se escribirá:

Si deseas ver el resultado click [aquí](https://codepen.io/gersongams/pen/WdKgGp).


```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Estilo interno</title>
    <style>
      h1 {
        color: yellow;
        background-color: black;
        border: 1px solid red;
      }

      p {
        color: white;
      }
    </style>
  </head>
  <body>
    <h1>Bienvenido al CoreUpgrade!</h1>
    <p>Este es un ejemplo de estilo interno</p>
  </body>
</html>
```

### Hoja de estilo externa

Un CSS externo es cuando el CSS se encuentra en un archivo separado con una extensión .css, y lo referenciamos desde HTML con un elemento <link>. 

El archivo HTML se parecerá a lo siguiente:

Si deseas ver el resultado click [aquí](https://codepen.io/gersongams/pen/BJPOWL).

Archivo index.html

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Estilo externo</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <h1>Bienvenido al CoreUpgrade!</h1>
    <p>Este es un ejemplo de estilo externo</p>
  </body>
</html>
```

Archivo style.css

```css
h1 {
    color: yellow;
    background-color: black;
    border: 1px solid red;
}

p {
    color: white;
}
```
