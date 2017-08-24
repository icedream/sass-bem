# sass-bem
Implement the BEM naming convention for stylesheets using Sass.

## Installation

### NPM

Installation in any project is as simple as running this command:

    npm install -S sass-bem

## Usage

### SCSS

```scss
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
