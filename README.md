# About

This grid system is a combination of the Semantic Grid System and Flexbox. It will give you the flexibility to create a semantic grid system while using all of Flexboxes features.

The examples provided in this README assume you are using autoprefixer.

## The Initial Setup
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

## The Flexbox Way

### The flexcolumn(); Mixin
HTML markup
```html
<div class="container">
	<div class="container-item"></div>
	<div class="container-item"></div>
</div>
```

SCSS
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

## The Non-Flexbox Way

### The column(); Mixin
HTML markup
```html
<div class="container">
	<div class="container-item"></div>
	<div class="container-item"></div>
</div>
```

SCSS
```scss
.container{
	@include row;

	&-item{
		@include column(4);

		&:nth-of-type(1){
			@include push(2);
		}

		&:nth-of-type(2){
			@include pull(2);
		}
	}
}
```

Compiled CSS
```CSS
.portfolio{
	display: block;
  margin: 0 auto;
  width: 100%;
  max-width: 1400px;
}

.portfolio-item {
  display: inline-block;
  float: left;
  width: 30.95238%;
  margin: 0 1.19048%;
}

.portfolio-item:nth-of-type(1) {
  margin-left: 17.85714%;
}

.portfolio-item:nth-of-type(2) {
  margin-right: 17.85714%;
}
```

## Credits
[Philip Walton](http://philipwalton.github.io/solved-by-flexbox/) for 'Solved by Flexbox.'
[Tyler Tate](https://github.com/tylertate/semantic.gs) for 'The Semantic Grid System.'