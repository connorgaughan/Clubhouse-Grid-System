# About

This grid system is a combination of the Semantic Grid System and Flexbox. It will give you the flexibility to create a semantic grid system while using all of Flexboxes features.

The examples provided in this README assume you are using autoprefixer.

## The Initial Setup
Setting up the grid defaults.
```scss
//------------------------------------------------------------------------------
//  Grid Defaults - max-width of 1400px Wide
//  (12 columns * 80px) + (11 gutters * 40px) = 1400px
//------------------------------------------------------------------------------

$column-width: 80px;
$gutter-width: 40px;
$columns: 12;
$max-width: 1440px;
$total-width: 100%;
```

##The column(); Mixin
HTML markup
```html
<div class="container">
	<div class="container-item"></div>
	<div class="container-item"></div>
</div>
```

SCSS
```scss
// A mobile first approach
.container{
	@include row();

	&-item{
		@include column(12);

		@media screen and (min-width:46em){
			@include column(6);
		}
	}
}
```

## Live Demo
[Check out a live demo of this in action.](http://codepen.io/connorgaughan/full/jWWwQv/)