# Sass Helpers

## Table of Contents

- [Getting Started](#getting-started)
  * [Installation](#installation)
  * [Usage](#usage)
- [Examples](#examples)
  * [Breakpoints](#breakpoints)

A group of mixins, functions and variables to get your frontend project started.

## Getting Started

### Installation

`npm install starlette-sass-helpers`

### Usage

Include the following "import" in your sass files. 

```scss
@import "path/to/your/node_modules/starlette-sass-helpers/scss/abstracts/abstracts";
```

Remember to change out "path/to/your/" to match your folder structure.

For example, if your sass file is located at "/assets/sass/layout.scss" then the code would change to this:

```scss
@import "../../node_modules/starlette-sass-helpers/scss/abstracts/abstracts";
```

## Examples

### Breakpoints

```scss
body {
    @include breakpoint(sm) { 
        color: green;
    }
    @include breakpoint(sm, max) { 
        color: blue;
    }
    @include breakpoint(sm, between) {
        color: red;
    }
    @include breakpoint(lg, between) {
        color: black;
    }
}
```

The above code compiles to this

```css
@media(min-width: 576px) {
    body {
        color: green;
    }
}
@media(max-width: 575px) {
    body {
        color: blue;
    }
}
@media(min-width: 576px)and (max-width: 767px) {
    body {
        color: red;
    }
}
@media(min-width: 992px)and (max-width: 1199px) {
    body {
        color: #000;
    }
}
```