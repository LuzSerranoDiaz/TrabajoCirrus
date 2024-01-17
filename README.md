# Guía de uso Cirrus

## Estructura grid

En cirrus tenemos estas opciones para realizar una estructura de una pagina con grid.
Por defecto la pagina está dividida en 12 columnas y utilizamos distintas clases para posicionar los elementos en el *layout* que preferamos.

### * Columnas y filas
  Utilizando las clases grid-c- grid-r-, asigna el nº de columnas al elemento, y grid-cs/rs- y grid-ce/re-, para asignar donde empiezan y acaban los elementos en el grid.  
  
![row y col](https://github.com/LuzSerranoDiaz/TrabajoCirrus/assets/125549381/fe2add22-0abb-4dc6-b799-74ed0ca1c3e2)
```html
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

![colores](https://github.com/LuzSerranoDiaz/TrabajoCirrus/assets/125549381/0ee974cb-9fb9-4c2a-8930-23263c03f593)

## Espaciado

### Padding

Para poner padding en un elemento se utiliza la clase `p-*`, las clases `py-*, px-*` para añadir padding arriba y abajo y a los lados respectivamente y las clases `pt-* (top), pb-* (bottom), pl-* (left) y pr-* (right)` para añadir padding únicamente a un lado.

Los tamaños van desde 0 a 64, cada punto valiendo 0.5rem. 
Por ejempplo `pt-4` daría un padding top de 2 rem.

### Margin
Margin funciona exactamente igual a padding pero con la letra m en vez de la letra p en las clases, `mt-*`

## Botones

Hay 4 maneras de crear un boton en cirrus
```html
<button>Button</button>
<div class="btn">Button</div>
<input type="submit" value="Submit">
<a class="btn">Button</a>
```
![botones](https://github.com/LuzSerranoDiaz/TrabajoCirrus/assets/125549381/6d266f19-0251-4ac3-8078-6eb369eff56f)

Sus tamaños pueden variar según la clase:

![botonesTamaño](https://github.com/LuzSerranoDiaz/TrabajoCirrus/assets/125549381/8ccea822-b342-4a6e-858b-972e0aad0fe7)


### Grupos de botones
En cirrus se pueden agrupar botones utilizando un div con la clase `btn-group` y dentro botones (solo la etiqueta `<button>` funciona con esto).
```html
<div class="btn-group">
    <button class="btn-primary">First Button</button>
    <button class="btn-primary">Second Button</button>
    <button class="btn-primary">Third Button</button>
</div>
```
![btngroup](https://github.com/LuzSerranoDiaz/TrabajoCirrus/assets/125549381/12fe58e1-3f56-4632-a90b-4e9ebeb20b90)

### Variaciones
Boton animado `btn-animated`, le da un pequeño bote al presionarlo

Boton desactivado, con el atributo `disabled` en los botones `input` y `<button>`, o poner en el nodo texto de las etiquetas `a` y `div` 'disabled'
```html
<button class="btn-info btn--disabled">Disabled</button>
<div class="btn btn-info btn--disabled">Disabled</div>
<input class="btn-info" type="submit" disabled value="Submit Disabled" />
<a href="#" class="btn btn-info btn--disabled">Disabled</a>
```

Boton cargando, con las clases `animated loading`.

`<button class="animated loading hide-text">123</button>`

Boton de cerrar, con las clases `frame btn-close`

`<button class="btn-close u-pull-right"></button>`

## Header 

El header tiene una estructura que se puede explicar con este ejemplo

```html
<div class="header header-fixed u-unselectable header-animated">
```
La clase `header` sirve como root y conntenedor de todo el header.
```html
    <div class="header-brand">
        <div class="nav-item no-hover">
            <a><h6 class="title">Logo</h6></a>
        </div>
```
La clase `header-brand` es el contenedor más a la izquierda donde se suele poner el logo.
```html
        <div class="nav-item nav-btn" id="header-btn">
            <span></span>
            <span></span>
            <span></span>
        </div>
    </div>
```
La clase `nav-item` es para todos los elementos del nav.
```html
    <div class="header-nav" id="header-menu" role="button">
```
La clase `header-nav` está diseñada para añadir links, menus y otros componentes. En tablets y smartphones estos no aparecen.
```html
        <div class="nav-left">
```
`nav-left` es el contenedor más a la izquierda del `header-nav`
```html
            <div class="nav-item text-center">
                <a href="#">
                    <span class="icon">
                        <i class="fab fa-wrapper fa-github" aria-hidden="true"></i>
                    </span>
                </a>
            </div>
            <div class="nav-item text-center">
                <a href="#">
                    <span class="icon">
                        <i class="fab fa-wrapper fa-slack" aria-hidden="true"></i>
                    </span>
                </a>
            </div>
            <div class="nav-item text-center">
                <a href="#">
                    <span class="icon">
                        <i class="fab fa-wrapper fa-twitter" aria-hidden="true"></i>
                    </span>
                </a>
            </div>
            <div class="nav-item has-sub toggle-hover" id="left-dropdown">
                <a class="nav-dropdown-link">Animated</a>
                <ul class="dropdown-menu dropdown-animated" role="menu">
                    <li role="menuitem"><a href="#">First Item</a></li>
                    <li role="menuitem"><a href="#">Second Item</a></li>
                    <li role="menuitem"><a href="#">Third Item</a></li>
                </ul>
            </div>
        </div>

        <div class="nav-right">
            <div class="nav-item active">
                <a href="#">Active</a>
            </div>
            <div class="nav-item">
                <a href="#">Link 1</a>
            </div>
            <div class="nav-item has-sub" id="right-dropdown">
                <a class="nav-dropdown-link">Click Me</a>
                <ul class="dropdown-menu" role="menu">
                    <li role="menuitem"><a href="#">First Item</a></li>
                    <li role="menuitem"><a href="#">Second Item</a></li>
                    <li role="menuitem"><a href="#">Third Item</a></li>
                    <li class="dropdown-menu-divider"></li>
                    <li role="menuitem"><a href="#">Fourth Item</a></li>
                </ul>
```
La clase `nav-dropdown-link` especifica que el link dentro del `nav-item` está asociado a un `dropdown-menu`.
`dropdown-menu` es el menú `ul`, la clase solo sirve para asociarlo al `nav-dropdown-link`.
`dropdown-mennu-divider` se utiliza para dividir los componentes del menú.
```
            </div>
        </div>
    </div>
</div>
```

![header](https://github.com/LuzSerranoDiaz/TrabajoCirrus/assets/125549381/e785499f-1097-4cc6-b50a-ceddf913c662)


## Footer


```html
<footer class="footer">
```
La clase `footer` sirve como contenedor de los elementos footer con un padding de 6 rem arriba y abajo.
```html
    <h6 class="footer__title text-white uppercase">Logo</h6>
```
La clase `footer_title` es un titulo estandar con un borde abajo.
```html
    <div class="content">
        <div class="divider"></div>

        <div class="row">
            <div class="col-4">
                <ul class="no-bullets">
                    <a href="!#">
                        <li class="footer__list-item">Home</li>
                    </a>
                    <a href="!#">
                        <li class="footer__list-item">Sign Up</li>
                    </a>
                    <a href="!#">
                        <li class="footer__list-item">Downloads</li>
                    </a>
                    <ul>
                    </ul>
                </ul>
            </div>
```
La clase `footer_list-item` da unos estilos por defecto a los elementos de lista.
```html
            <div class="col-4">
                <ul class="no-bullets">
                    <a href="!#">
                        <li class="footer__list-item">Company Information</li>
                    </a>
                    <a href="!#">
                        <li class="footer__list-item">Contact Us</li>
                    </a>
                    <a href="!#">
                        <li class="footer__list-item">Reviews</li>
                    </a>
                    <ul>
                    </ul>
                </ul>
            </div>
            <div class="col-4">
                <ul class="no-bullets">
                    <a href="!#">
                        <li class="footer__list-item">FAQ</li>
                    </a>
                    <a href="!#">
                        <li class="footer__list-item">Help Desk</li>
                    </a>
                    <a href="!#">
                        <li class="footer__list-item">Forums</li>
                    </a>
                    <ul>
                    </ul>
                </ul>
            </div>
        </div>
    </div>
    <p class="subtitle">Company © 2018.</p>
</footer>
```
![footer](https://github.com/LuzSerranoDiaz/TrabajoCirrus/assets/125549381/891d66ae-cb42-41c5-bb47-52e1398b5ebf)


## Menus

```html
<ul class="menu">
  <li class="menu-item selected">
    <a>One</a>
  </li>
  <li class="menu-item">
    <a>Two</a>
  </li>
  <li class="menu-item">
    <a>Three</a>
  </li>
</ul>
```
