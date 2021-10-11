### 🕶 Responsive grid system Sass based similar to the bootstrap grid system.

## Installation
```
npm install sass-grid-system
```

## Usage

```html
<div class="container">
    <div class="row">
        <div class="col-6"></div>
        <div class="col-6"></div>
    </div>
</div>
```

## Fluid container

```html
<div class="container-fluid">
    <div class="row">
        <div class="col-6"></div>
        <div class="col-6"></div>
    </div>
</div>
```

## Nesting
#### You can nest rows inside columns.

```html
<div class="container">
    <div class="row">
      <div class="col-6">
        Level 1: .col-6
      </div>
      <div class="col-6">
        <div class="row">
          <div class="col-4">
            Level 2: .col-4
          </div>
          <div class="col-4">
            Level 2: .col-4
          </div>
          <div class="col-4">
            Level 2: .col-4
          </div>
        </div>
      </div>
    </div>
</div>
```
![Nested Grid Image](https://www.dropbox.com/s/rsb0mwy5yw8j46q/sass_grid_nested.png?raw=1)

## Grid options

| Size   | Prefix  | Breakpoint |  .container max-width |
|--------|---------|--------|-----------------------|
| Small  | .col-sm | ≥576px | 540px                 |
| Medium | .col-md | ≥768px | 732px                 |
| Large  | .col-lg | ≥992px | 956px                 |
| Extra large  | .col-xl | ≥1200px | 1164px                 |

## Customize _var.scss

##### By default the grid system has 4 breakpoints, 12 columns and default names to selectors and prefixes, but you can customize it all.

```scss
$columns: 12; //---> Number of columns
$gutter: 1.6%; //---> The space between the columns in percentage
```

##### Change selectors name

```scss
$selectors: (
    container: '.container', //---> Eg.: you can change to .section and work with class="section" and class="section-fluid" instead of class="container" or class="container-fluid"
    row: '.row',
    column: '.col'
);
```

##### By default the grid works with 576px, 768px, 992px and 1200px breakpoints. But you can add, remove or change the values to customize your own breakpoints. sm, md, lg, xl are the prefixes used in the selector eg.: .col-md-12.
##### Eg.: you can change sm to s and work with class="col-s-1" if you want.

```scss
$breakpoints: (
    sm: 576px, //---> [prefix name : breakpoint value]
    md: 768px,
    lg: 992px,
    xl: 1200px
);
```

![Grid 12 Columns image](https://www.dropbox.com/s/4py3acqej1vr084/sass_grid_1.png?raw=1)

[Created by WillianSMonteiro](https://github.com/wmonteiro)

## License

MIT
