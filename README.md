# Sass Helpers

## Table of Contents

- [Getting Started](#getting-started)
  * [Installation](#installation)
  * [Usage](#usage)
- [Examples](#examples)
  * [Breakpoints](#breakpoints)
  * [Flexbox](#flexbox)
  * [Grid](#grid)

A group of mixins, functions and variables to get your frontend project started.

## Getting Started

### Installation

```cmd
npm install starlette-sass-helpers
```

### Usage

Include the following "import" in your sass files. 

```scss
@import "path/to/your/node_modules/starlette-sass-helpers/scss/sass-helpers";
```

Remember to change out "path/to/your/" to match your folder structure.

For example, if your sass file is located at "/assets/sass/layout.scss" then the code would change to this:

```scss
@import "../../node_modules/starlette-sass-helpers/scss/sass-helpers";
```

## Documentation

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

### Flexbox

See [how flexbox works](https://developer.mozilla.org/en-US/docs/Glossary/Flexbox). 

```scss
body {
    @include flexbox;
    @include flex-direction( column );
}
```

![New Feature](https://user-images.githubusercontent.com/19154356/124391000-9c725d80-dcee-11eb-953f-4044ca557752.png)

### Grid

Uses a 24 grid column structure.

`column-1` is the smallest size column (4.16%).

![](https://user-images.githubusercontent.com/19154356/124390915-22da6f80-dcee-11eb-859b-6268b143a8e9.png)

```html
<div class="container">
	<div class="row">
		<div class="column-1"> 1 </div>
		<div class="column-2"> 2 </div>
		<div class="column-3"> 3 </div>
		<div class="column-4"> 4 </div>
		<div class="column-5"> 5 </div>
		<div class="column-6"> 6 </div>
		<div class="column-7"> 7 </div>
		<div class="column-8"> 8 </div>
		<div class="column-9"> 9 </div>
		<div class="column-10"> 10 </div>
		<div class="column-11"> 11 </div>
		<div class="column-12"> 12 </div>
		<div class="column-13"> 13 </div>
		<div class="column-14"> 14 </div>
		<div class="column-15"> 15 </div>
		<div class="column-16"> 16 </div>
		<div class="column-17"> 17 </div>
		<div class="column-18"> 18 </div>
		<div class="column-19"> 19 </div>
		<div class="column-20"> 20 </div>
		<div class="column-21"> 21 </div>
		<div class="column-22"> 22 </div>
		<div class="column-23"> 23 </div>
		<div class="column-24"> 24 </div>
	</div>
</div>
```

#### Responsive
