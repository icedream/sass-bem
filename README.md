# sass-bem
Implement the BEM naming convention for stylesheets using Sass.

## Installation

### NPM

Installation in any project is as simple as running this command:

    npm install -S sass-bem

## Configuration

The code can be configured to use different separators or to implement
shorthands for all mixins. Look at [src/\_variables.sass](src/_variables.sass) to find out what variables can be tweaked for this.

## Usage

Examples below assume to be part of an npm project with Webpack and sass-loader set up with this package installed.

### SCSS

```scss
@import "~sass-bem"

// Block called "menu"
@include block(menu) {
    display: flex;
    width: 100%;

    // Element called "button" in the "menu" block
    @include element(button) {
        border-radius: 4px;
        padding: 8px;
        text-align: center;

        // Modifier called "dark" for the menu button
        @include modifier(dark) {
            background-color: #333;
            color: #fff;
        }
    }
}
```

### Sass

```sass
@import ~sass-bem

// Block called "menu"
+block(menu)
    display: flex
    width: 100%

    // Element called "button" in the "menu" block
    +element(button)
        border-radius: 4px
        padding: 8px
        text-align: center

        // Modifier called "dark" for the menu button
        +modifier(dark)
            background-color: #333
            color: #fff
```
