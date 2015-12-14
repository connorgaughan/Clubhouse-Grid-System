# About

This grid system is a combination of the Semantic Grid System and Flexbox. It will give you the flexibility to create a semantic grid system while using all of Flexboxes features.

## How to Use

### The Grid System Setup
```scss
// Import Flexbox Mixins
@import "flexbox";

//------------------------------------------------------------------------------
//  Grid Defaults - max-width of 1400px Wide
//  (12 columns * 80px) + (11 gutters * 40px) = 1400px
//------------------------------------------------------------------------------
$column-width: 100px;
$gutter-width: 40px;
$columns: 12;
$max-width: 1400px;
$total-width: 100%;
```

## Credits
[Philip Walton](http://philipwalton.github.io/solved-by-flexbox/) for 'Solved by Flexbox.'
[Tyler Tate](https://github.com/tylertate/semantic.gs) for 'The Semantic Grid System.'