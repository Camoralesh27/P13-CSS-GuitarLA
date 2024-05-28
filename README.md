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