# Guía de uso Cirrus

## Estructura grid

En cirrus tenemos estas opciones para realizar una estructura de una pagina con grid.
Por defecto la pagina está dividida en 12 columnas y utilizamos distintas clases para posicionar los elementos en el *layout* que preferamos.

### Columnas y filas
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

Con las clases `menu` y `menu-item` en una lista podemos realizar un menu.

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

![menu1](https://github.com/LuzSerranoDiaz/TrabajoCirrus/assets/125549381/567bc4ef-1add-43a0-80af-47c896e6b4b4)

También se pueden hacer menus dropdown con la clase `list-dropdown`.

```html
<div class="list-dropdown">
    <div class="btn-group">
        <button class="btn-primary">Dropdown</button>
        <button class="btn-primary btn--sm btn-dropdown"><i class="fa fa-wrapper fa-caret-down" aria-hidden="true"></i>
        </button>
        <ul class="menu">
            <li class="menu-item"><a href="#">Google Chrome</a></li>
            <li class="menu-item"><a href="#">Firefox</a></li>
            <li class="menu-item"><a href="#">Polarity</a></li>
        </ul>
    </div>
</div>
```

## Media

### Imagenes

Con la clase `img-stretch` se hace la imagen responsiva.
`<img class="img-stretch" src="img/gallina.png">`

Con la clase `img-cover` y `img-contain` para hacer que la imagen ocupe su nodo padre entero.
`<img class="img-contain" src="img/gatoPanchi.jpg" style="background: rgb(238, 238, 238); height: 350px;">`

Con cirrus se pueden crear un elemento llamado `figures` que son contenedores que se posicionan independientemente del resto de la pagina.
Para crearlos se contiene la imagen en una etiqueta `<figure>` con la clase `fig`.
```html
<figure class="fig">
    <img src="img/yosemite-falls.png" />
    <figcaption class="fig-caption u-text-center">
        Yosemite Valley, United States
    </figcaption>
</figure>
```

### Videos

Igual que la imagen se puede hacer responsivo el video con la clase `media-stretch`.

Y se puede cambiar el 'ratio' de un video con las clases `rat-4-3` y `rat-1-1` para poner los videos en resolución 4:3 y 1:1.

```html
<div class="media-stretch rat-1-1">
    <iframe width="560" height="315" src="./..." frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div>
```

Y con la clase `video-fullscreen` para hacer que ocupe toda la pantalla.

## Formularios

### Checkboxes

Para estilizar con cirrus los checkboxes se utilizan las clases `form-ext-control form-ext-checkbox` en el elemento contenedor del checbox, `form-ext-input` en el elemento input y `form-ext-label` en el elemento label.

```html
<div class="form-ext-control form-ext-checkbox">
    <input id="check1" class="form-ext-input" type="checkbox" disabled="">
    <label class="form-ext-label" for="check1">Unchecked</label>
</div>
```

Se pueden seleccionar los colores v1 con las clases `form-ext-input--*`.

```html
<div class="form-ext-control form-ext-checkbox">
    <input id="check-dark" class="form-ext-input form-ext-input--dark" type="checkbox" checked />
    <label class="form-ext-label" for="check-dark">dark</label>
</div>
```

### Inputs

Cada input viene estilada por defecto pero podemos cambiarlo en pequeñas maneras.

Tamaños:
Podemos cambiar los tamaños con la clase `input-*` * siendo `xs, sm, md, lg, xl`.

![inputSize](https://github.com/LuzSerranoDiaz/TrabajoCirrus/assets/125549381/21ede3c2-44b5-41f6-b099-fbaaf177e0cb)

Estados:
Se pueden cambiar el estado de cada input con estas clases en el atributo `placeholder`

```html
<div class="input-control">
<input disabled type="text" placeholder="Disabled state" />
</div>
```

Todos los estados son `Normal state, Focused state, Disabled state, Success state, Error state`

### Labels

Se puede utilizar la clase `info` para poner un 'footnote'.

```html
<div class="col-lg-6">
    <label>Regular Label</label>
    <input type="text" placeholder="The label above is a regular label." />
    <span class="info u-text-center">I am using the <code>info</code> class.</span>
</div>
```
![footnote](https://github.com/LuzSerranoDiaz/TrabajoCirrus/assets/125549381/602e5a28-0106-4a9d-8484-3716f7b82b5b)

### Radio

Son checkboxes redondas, se aplican todas las mismas clases.

### Toggle

Para formar un toggle se utilizan las clases `form-ext-toggle__label` en la etiqueta label, `formt-ext-toggle` en el contenedor del toggle y `form-ext-toggle__toggler` en un div con el icono de toggle.

```
<div class="form-ext-control">
    <label class="form-ext-toggle__label"><span>Toggle off</span>
        <div class="form-ext-toggle">
            <input name="toggleCheckbox" type="checkbox" class="form-ext-input" />
            <div class="form-ext-toggle__toggler"><i></i></div>
        </div>
    </label>
</div>
```

Tiene las mismas capacidades de estilo que los checboxes.

## Elementos

Cirrus tiene una gran cantidad de elementos para la estructura de la pagina web, aquí se mostrarán los más importantes.

### Cards

Las cards funcionan de la misma manera que en bootstrap.

```
<div class="card" style="max-width: 350px;">
```
La clase `card` sirve para definir el elemento contenedor.
```html
    <div class="card__container">
        <div class="card__image"></div>
        <div class="card__title-container">
            <p class="title">Title</p><span class="subtitle">Subtitle</span>
        </div>
    </div>
```
Las clases `card__container` declara el contenido de la carta en sí,
`card__image` la imagen principal de la card
y `card__title-container` es el contenedor del titulo y subtitulo de la card.
```html
    <div class="content">
        <p>Text and other content belong here, inside a <code>content</code> div.</p>
    </div>
```
La clase `content` define el cuerpo de la card.
```html
    <div class="card__action-bar u-center">
        <button class="btn-link outline">Buttons</button>
        <button class="btn-link outline">Go here</button>
    </div>
```
La clase `card__action-bar` define la parte de la carta donde se pueden insertar botones u otros elementos interactuables.
```html
    <div class="card__footer">
        <div class="u-text-center"><span>This is additional footer text in <code>card__footer</code>.</span></div>
    </div>
</div>
```
Y la clase `card__footer` define el footer de la card.

![card](https://github.com/LuzSerranoDiaz/TrabajoCirrus/assets/125549381/6612a006-3a75-4a7e-af1d-367b7fd43d46)

#### Card animada

Para realizar una card animada se tiene que poner la clase `card--slide-up` junto a la clase `card` en el div contenedor.
`<div class="card card--slide-up">`
La clase `card__title-container` se sustituye por la clase `card__mobile-title`.
```html
 <div class="card__mobile-title">
        <div class="content">
            <div class="tile">
                <div class="tile__container">
                    <p class="tile__title">Kangaroo Valley Safari</p>
                    <p class="tile__subtitle">By John Doe</p>
                </div>
            </div>
        </div>
    </div>
```
El cuerpo se situa ahora en un div con las clases `card__body content`
`<div class="card__body content">`

### Avatar

Los avatares son una manera de implementar una imagen en distintos elementos de manera más personal.
```html
<div class="avatar"><img src="..." alt="avatar"></div>
```

![avatar](https://github.com/LuzSerranoDiaz/TrabajoCirrus/assets/125549381/86568f10-e116-456b-85a6-e3b1c442b3cd)

Tambien se pueden poner con texto utilizando el atributo `data-text`.

```html
<div class="avatar text-gray-000" data-text='Aa'></div>
```

Y se le pueden cambiar el tamaño con las clases `avatar--xs, avatar--sm, avatar--lg,` y `avatar--xl.`
```html
<div class="avatar avatar--xs" data-text="Jz"></figure>
```

### BreadCrumbs

Breadcrumbs es una lista indicando donde te situas actualmente dentro de la pagina web.

![breadcrumbs](https://github.com/LuzSerranoDiaz/TrabajoCirrus/assets/125549381/9cc57ca9-8ab4-4578-8ad8-b224bfdf4076)

Es muy sencillo de crear es una lista con las clases `breadcrumb` en el contenedor de los elementos y `breadcrumb__item` en los elementos de la lista.
Tambien se utiliza la clase `breadcrumb__item--active` para indicar el elemento 'activo' o en el que se situa ahora mismo el usuario.

```html
<ul class="breadcrumb">
    <li class="breadcrumb__item">
        <a href="#">Home</a>
    </li>
    <li class="breadcrumb__item">
        <a href="#">Settings</a>
    </li>
    <li class="breadcrumb__item breadcrumb__item--active">
        <a href="#">Change Avatar</a>
    </li>
</ul>
```
Tambien se puede influenciar el posicionamiento con las clases `breadcrumb--center` para posicionarlo en el centro y `breadcrumb--right` para posicionarlo en la derecha.
```html
<ul class="breadcrumb breadcrumb--right">
<ul class="breadcrumb breadcrumb--center">
```

Y se pueden seleccionar los separadores con la clase `bradcrumb--(arrow, bullet, dot, gt)`

```html
<ul class="breadcrumb breadcrumb--gt">
<ul class="breadcrumb breadcrumb--arrow">
<ul class="breadcrumb breadcrumb--bullet">
<ul class="breadcrumb breadcrumb--dot">
```

![bcgt](https://github.com/LuzSerranoDiaz/TrabajoCirrus/assets/125549381/1dbebb7f-840e-4e91-984d-ccd6cbf2c1c3)

### Tiles

Tiles son alternativas a cards, y suelen ser más usadas en smartphones.

```html
<div class="tile">
    <div class="tile__icon">
        <figure class="avatar"><img src="https://www.seoclerk.com/pics/319222-1IvI0s1421931178.png"></figure>
    </div>
    <div class="tile__container">
```
Las clases principales de un tile son:
`tile` que indica al div contenedor que es un tile.
`tile__icon` que es la imagen que se sitúa como avatar.
`tile__container` que indica el cuerpo del tile.
```html
        <p class="tile__title m-0">Robert Downey Jr. shared a post from <b>Stark Industries</b>.</p>
        <p class="tile__subtitle m-0">Robert shared: 'Stark Industries is proud to announce its brand new suit.'</p><span class="info">23 minutes ago</span>
```
las clases `tile__title` indica el titulo del tile y `tile__subtitle` el subtitulo.
```html
        <div class="tile__buttons m-0">
```
La clase `tile__buttons` indica el div contenedor de los botones.
```html
            <button class="btn-primary btn--sm uppercase">View</button>
            <button class="btn--sm uppercase">Dismiss</button>
        </div>
    </div>
</div>
```

![tile](https://github.com/LuzSerranoDiaz/TrabajoCirrus/assets/125549381/0dddfcd9-cb5a-425d-a1f9-605798a92824)

### Toasts

Los toasts de cirrus son las alerts de bootstrap, tienen la misma funcionalidad.

La única clase necesaria para formar un toast es la clase `toast` en el div contenedor, junto al `toast__title` si se requiere un titulo y `toast--*` para seleccionar un color.

```html
<div class="toast toast--primary">
    <button class="btn-close"></button>
    <h4 class="toast__title">Danger!</h4>
    <p>Run.</p>
</div>
```

![run](https://github.com/LuzSerranoDiaz/TrabajoCirrus/assets/125549381/ace629ab-b5e4-49e2-8762-e00e4eac0ea6)


Para incluir un boton de cerrado se utiliza.
```html
<button class="btn-close"></button>
```
![close](https://github.com/LuzSerranoDiaz/TrabajoCirrus/assets/125549381/8bb59046-e944-47c3-8449-4a17614cb150)


