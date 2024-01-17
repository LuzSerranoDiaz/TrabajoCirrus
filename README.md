# Guía de uso Cirrus

## Estructura grid

En cirrus tenemos estas opciones para realizar una estructura de una pagina con grid.
Por defecto la pagina está dividida en 12 columnas y utilizamos distintas clases para posicionar los elementos en el *layout* que preferamos.

### * Columnas y filas
  Utilizando las clases grid-c- grid-r-, asigna el nº de columnas al elemento, y grid-cs/rs- y grid-ce/re-, para asignar donde empiezan y acaban los elementos en el grid.  
  
![row y col](https://github.com/LuzSerranoDiaz/TrabajoCirrus/assets/125549381/fe2add22-0abb-4dc6-b799-74ed0ca1c3e2)
```
<div class="grid grid-rows-3 grid-cols-2 grid-flow-col u-gap-2 font-bold">
  <div class="u-text-center p-2 u-round-xs bg-orange-200 text-orange-700">1</div>
  <div class="u-text-center p-2 u-round-xs bg-orange-200 text-orange-700">2</div>
  <div class="u-text-center p-2 u-round-xs bg-orange-200 text-orange-700">3</div>
  <div class="u-text-center p-2 u-round-xs bg-orange-200 text-orange-700">4</div>
  <div class="u-text-center p-2 u-round-xs bg-orange-200 text-orange-700">5</div>
</div>
```
### Viewports

Para poder hacer los elementos reponsivos utilizamos las clases `xs, sm, md, lg y xl`.

![col sm](https://github.com/LuzSerranoDiaz/TrabajoCirrus/assets/125549381/ffa7cc7c-e85e-437f-b52b-6b7c4efb3acb)

## Colores

Los colores de cirrus a diferencia de bootstrap se realizan seleccionando un color base y luego su intensidad.
`bg-(color)-(100-900)`
Los colores base de cirrus son `pink, red, orange, yellow, green, teal, blue indigo, purple y grey`
