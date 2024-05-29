# Notas del proyecto.

## Selector de atributo.

Selecciona **todos los que tengan en algun lugar** 'contenedor', ya sea antes ó descpues.
```css
[class*="contenedor"] {
}
```

Selecciona todos los que **inician** con 'contenedor'.
```css
[class^="contenedor"] {
}
```

Selecciona todos los que **finalizan** con 'contenedor'.
```css
[class$="contenedor"] {
}
```

En nuestro caso el adecuado fue el siguiente ya que estamos utilizando BEM, seleccionando todos los que **finalizan** con '__contenedor'.
```css
[class$="__contenedor"] {
}
```

## Cortar contenido de un texto muy grande para que aparezca con 4 puntos 
Te crea como un pseudo elemento con una elipsis al final.
No te genera más contenido pero da un máximo y lo corta, por ello hay que . 

```css
.entrada__texto {
    /* crea una caja */
    display: -webkit-box;
    /* la orientación es vertical */ 
    -webkit-box-orient: vertical;
    /* queremos que corte 4 lineas */
    -webkit-line-clamp: 4;
    /* el contenido sobrante lo oculta */
    overflow: hidden;
}
```