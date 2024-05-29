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

## border y outline en "select" de form

```css
.producto__cantidad {
    border: 2px solid var(--primary);
}

.producto__cantidad:focus-visible {
    outline: 2px solid var(--primary);
    border: none;
}
```
El focus visible es el border al rededor del **select**, pero para que no se empalmen los 2 por eso quitamos el border al momento de activarse **focus-visible**.

## display flex
Display flex actua tomando todo el ancho de su contenedor. Así le hicimos en producto.html para que el solect tomara todo el ancho del contenedor.

```css 

.producto__formulario {
    /* Hace que se extienda en todo el bloque */
    display: flex;
    flex-direction: column;
    
}

```