<p align="center"><img src="Sass_Logo_Color.svg" width="400"></p>

<p align="center">Creating a simple docs of <a href="https://sass-lang.com">👉 SASS (Syntactically Awesome Style Sheets) 👈</a></p>

<p align="center">
    <a href="https://opensource.org/licenses/MIT">
        <img alt="License" src="https://img.shields.io/badge/License-MIT-yellow.svg">
    </a>
    <a href="#">
        <img alt="License" src="https://img.shields.io/github/last-commit/MagicalStrangeQuark/SASS">
    </a>
    <a href="#">
        <img alt="License" src="https://img.shields.io/github/followers/MagicalStrangeQuark?style=social">
    </a>
</p>

<h6 align="center">Installation</h6>

```bash
    sudo npm install -g sass
```

<p align="center"><a href="https://www.sassmeister.com">📩 SASS Meister 📩</a></p>

<h6 align="center">Compile Sass</h6>

<h6 align="center">Sass</h6>

```sass
    h1 {
        color: red;
    }
```

<h6 align="center">Sass to Scss</h6>

```sass
    sass main.sass main.scss
```

<h6 align="center">Scss to Css</h6>

```sass
    sass main.scss main.css
```

<h6 align="center">Scss</h6>

```sass
    h1 {
        color: red;
    }
```

<h6 align="center">Variables</h6>

```sass
    $color: black;

    h1 {
        color: $color;
    }

    h2 {
        color: $color;
        font-size: 2rem;
    }
```

<h6 align="center">Watch Files/Folders</h6>

```sass
    sass --watch <origin>:<target>
```

```sass
    sass --watch main.scss:main.css
```

<h6 align="center">Aninhamento</h6>

```css
    @charset "UTF-8";
    
    #conteudo {
        background: green;
        padding: 15px;
    }

    #conteudo h1, h2 {
        color: black;
    }

    #conteudo a {
        color: red;
    }

    #conteudo a:hover {
        color: yellow;
    }

```

```sass
    #conteudo {
        background: green;
        padding: 15px;

        h1, h2 {
            color: black;
        }

        a {
            color: red;

            &:hover {
                color: yellow;
            }
        }
    }
```

<h6 align="center">Scope</h6>

```sass
    $default-color: blue;

    h1 {
        $default-color: red;

        background-color: $default-color; /* red */
    }

    h2 {
        background-color: $default-color; /* blue */
    }
```

```sass
    $default-color: blue;

    h1 {
        $default-color: red !global;

        background-color: $default-color; /* red */
    }

    h2 {
        background-color: $default-color; /* red */
    }
```

<h6 align="center">Interpolation</h6>

```sass
    $class: red;
    $color: color;

    .#{$color} {
        #{$color}: $class;
    }
```

```css
    @charset "UTF-8";

    .color {
        color: red;
    }
```

<h6 align="center">For</h6>

```sass
    @for $i from 1 through 3 {
        .item-#{$i} {
            color: black;
        }
    }
```

```sass
    @for $i from 1 to 3 {
        .item-#{$i} {
            color: black;
        }
    }
```

<h6 align="center">While</h6>

```sass
    $counter: 0;

    @while ($counter < 5) {
        .list-item-#{$counter} {
            background-color: green;
        }
        
        $counter: $counter + 1;
    }
```

<h6 align="center">Each</h6>

```sass
    $list: green, black, yellow, white, gray;
    $counter: 0;

    @each $color in $list {
        div-#{$counter} {
            background-color: $color;
        }

        $counter: $counter + 1;
    }
```

<h6 align="center">Functions</h6>

```sass
    $total: 12;

    @function column-width($column: 0) {
        @return ($column / $total);
    }

    @function perc-column-width($column: 0) {
        @return column-width($column) * 100;
    }

    @function perc-string-column-width($column: 0) {
        @return percentage(column-width($column));
    }

    $result-abs: column-width(3);

    $result-perc: perc-column-width(3);

    $result-perc-string: perc-string-column-width(3);

    /* #{$result-abs} */

    /* #{$result-perc} */

    /* #{$result-perc-string} */
```

```sass
    .alert {
        background: mix(blue, green, 50%);
        color: black;
    }

    .alert {
        background: darken(green, 25%);
        color: black;
    }

    .alert {
        background: lighten(green, 50%);
        color: black;
    }
```

<h6 align="center">Importação</h6>

`Arquivos iniciando por underline não geram um .css, mas podem ser importados e usados por outras folhas de estilo.`

```bash
    .
    ├── css
    │   ├── main.css
    │   └── main.css.map
    └── scss
        ├── main.scss
        └── _styles.scss

    2 directories, 7 files
```

```sass
    @import "<filename>.scss";

    ...
```

```sass
    sass scss css
```

<h6 align="center">Mixin</h6>

```sass
    @mixin titulo ($color, $bg-color) {
        color: $color;
        background-color: $bg-color;
        padding: 10px 5px;
    }

    h1 {
        @include titulo (white, gray);
    }

    h2 {
        @include titulo (green, blue);
    }
```

<h6 align="center">Herança</h6>

```sass
    .parent-one {
        background: green;
    }

    .parent-two {
        color: blue;
    }

    .child {
        @extend .parent-one;
        @extend .parent-two;
    }
```