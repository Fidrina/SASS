<p align="center"><img src="Sass_Logo_Color.svg" width="400"></p>

<p align="center">Creating a simple page using <a href="https://sass-lang.com">👉 SASS (Syntactically Awesome Style Sheets) 👈</a></p>

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

<h6 align="center">Compile Sass</h6>

<h6 align="center">Sass</h6>

```sass
    h1
        color: red
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

<h6 align="center">Watch</h6>

```sass
    sass --watch <origin>:<target>
```

```sass
    sass --watch main.scss:main.css
```