# About

This grid system is a combination of the Semantic Grid System and Flexbox. It will give you the flexibility to create a semantic grid system while using all of Flexboxes features.

The examples provided in this README assume you are using autoprefixer.

## How to Use

### The Grid System Setup
Setting up the grid defaults.
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
### Using the Flexcolumn Mixin
The HTML markup
```html
<div class="container">
	<div class="container-item"></div>
	<div class="container-item"></div>
</div>
```

The SCSS
```scss
.container{
	@include flexrow;
	@include justify-content(center);

	&-item{
		@include flexcolumn(4);
	}
}
```

Compiled CSS
```CSS
.portfolio{
	display:-webkit-box;
	display:-webkit-flex;
	display:-moz-flex;
	display:-ms-flexbox
}

.portfolio-item{
	-webkit-flex-basis:31.11111%;
	-ms-flex-preferred-size:31.11111%;
	flex-basis:31.11111%;
	margin:0 1.11111%
}
```

## Credits
[Philip Walton](http://philipwalton.github.io/solved-by-flexbox/) for 'Solved by Flexbox.'
[Tyler Tate](https://github.com/tylertate/semantic.gs) for 'The Semantic Grid System.'