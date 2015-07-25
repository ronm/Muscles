
#Muscles
###Flex your Muscles
	
A CSS grid framework with a rich and easy to use api on top of the [Flexbox Layout Module](http://www.w3schools.com/cssref/css3_pr_flex.asp)
			
[Full Documentation and API](http://ronm.github.io/Muscles/)

Browser Support: [Can I Use](http://caniuse.com/#search=flex)
			
Some general use [templates](http://ronm.github.io/Muscles/demos/templates.html), jacked from [Zurb Foundation](http://foundation.zurb.com/templates.html).
			
####Links to some normally problematic layouts:
			
* [Holy Grail](http://ronm.github.io/Muscles/demos/holy-grail.html)
* [Sticky Footer](http://ronm.github.io/Muscles/demos/sticky-footer.html)
* [Sticky Footer (Alt)](http://ronm.github.io/Muscles/demos/sticky-footer-2.html)
* [Centered Content](http://ronm.github.io/Muscles/demos/centered-content.html)
			
##The Grid
			
```html
<div class="group">
	<div class="box-4"></div>
	<div class="box-4"></div>
	<div class="box-4"></div>
</div>
<div class="group">
	<div class="box-3"></div>
	<div class="box-6"></div>
	<div class="box-3"></div>
</div>
<div class="group">
	<div class="box-2"></div>
	<div class="box-8"></div>
	<div class="box-2"></div>
</div>
<div class="group">
	<div class="box-3"></div>
	<div class="box-9"></div>
</div>
<div class="group">
	<div class="box-4"></div>
	<div class="box-8"></div>
</div>
<div class="group">
	<div class="box-6 large-box-5"></div>
	<div class="box-6 large-box-7"></div>
</div>
<div class="group">
	<div class="box-6"></div>
	<div class="box-6"></div>
</div>
```

###Parent Level Sizing
			
To simplify, uniform sizing can be applied to all child elements by adding `.items-X` to the group.
			
```html
<div class="group items-3">
	<div class="box"></div>
	<div class="box"></div>
	<div class="box"></div>
	<div class="box"></div>
	<div class="box"></div>
	<div class="box"></div>	
</div>
```
			
			
			
###Nesting

Of course nesting is supported by adding `.group` to any descendant `.box` elements.

```html
<div class="group">
	<div class="group box-2">
		<div class="box"></div>
	</div>	
	<div class="group box-8">
		<div class="box-6"></div>
		<div class="box-6"></div>		
	</div>
	<div class="group box-2">
		<div class="box"></div>
	</div>	
</div>
```
			
			
###Auto Width

By not specifying a size on `.box` all elements will be equally sized along the main axis.

```html
<div class="group">
	<div class="box"></div>
	<div class="box"></div>
	<div class="box"></div>
</div>
```

```html
<div class="group">
	<div class="box"></div>
</div>
```

```html
<div class="group">
	<div class="box"></div>
	<div class="box"></div>
	<div class="box"></div>
	<div class="box"></div>
</div>
```

###Offsets

Offsets can also be used with `.offset-X`

```html
<div class="group">
	<div class="box offset-11"></div>
	<div class="box offset-10"></div>
	<div class="box offset-9"></div>
	<div class="box offset-8"></div>
	<div class="box offset-7"></div>
	<div class="box offset-6"></div>	
	<div class="box-7 offset-5"></div>
	<div class="box-8 offset-4"></div>
	<div class="box-9 offset-3"></div>
	<div class="box-10 offset-2"></div>
	<div class="box-11 offset-1"></div>
</div>
```
			
			
###Spacing
			
####Spacing along main axis (default: center)
			
Support for classes `.start`, `.end`, `.center`, `.between`, `.around`.			

```html
<div class="group start">
	<div class="box-2"></div>
	<div class="box-2"></div>
</div>
<div class="group end">
	<div class="box-2"></div>
	<div class="box-2"></div>
</div>
<div class="group center">
	<div class="box-2"></div>
	<div class="box-2"></div>
</div>
<div class="group between">
	<div class="box-2"></div>
	<div class="box-2"></div>
</div>
<div class="group around">
	<div class="box-2"></div>
	<div class="box-2"></div>
</div>
```		


####Spacing along cross axis (default: cross-center)

Classes `.cross-start`, `.cross-end`, `.cross-center`, `.cross-between`, `.cross-around`, `.cross-stetch`.
			
This class has no effect when there is only one line of content along the main axis.		

```html
<div class="group cross-start">
	<div class="box-12"></div>
	<div class="box-12"></div>
</div>
<div class="group cross-end">
	<div class="box-12"></div>
	<div class="box-12"></div>
</div>
<div class="group cross-center">
	<div class="box-12"></div>
	<div class="box-12"></div>
</div>
<div class="group cross-between">
	<div class="box-12"></div>
	<div class="box-12"></div>
</div>
<div class="group cross-around">
	<div class="box-12"></div>
	<div class="box-12"></div>
</div>
<div class="group cross-stretch">
	<div class="box-12"></div>
	<div class="box-12"></div>
</div>
```


###Alignment

####Alignment along cross axis (default: cross-align-center)

Classes `.cross-align-start`, `.cross-align-end`, `.cross-align-center`, `.cross-align-baseline`, `.cross-align-stetch`.
		
```html
<div class="group cross-align-start">
	<div class="box-2"></div>
	<div class="box-2"></div>
</div>
<div class="group cross-align-end">
	<div class="box-2"></div>
	<div class="box-2"></div>
</div>
<div class="group cross-align-center">
	<div class="box-2"></div>
	<div class="box-2"></div>
</div>
<div class="group cross-align-baseline">
	<div class="box-2"></div>
	<div class="box-2"></div>
</div>
<div class="group cross-align-stetch">
	<div class="box-2"></div>
	<div class="box-2"></div>
</div>
```
		
###Ordering

Element ordering can easily be achieved with `.order-X`.

`X` is natively supported up the the number of segments defined in the grid ( default : 12 ).

```html
<div class="group">
	<div class="box order-3">One</div>
	<div class="box order-1">Two</div>
	<div class="box order-2">Three</div>
	<div class="box order-4">Four</div>
</div>
```			

			
####First
			
The utility class of `.first` can be used to anchor items to the beginning of a group.

```html
<div class="group">
	<div class="box">One</div>
	<div class="box">Two</div>
	<div class="box first">Three</div>
</div>
```	

####Last
			
The utility class of `.last` can be used to push items to the end of a group.		

```html
<div class="group">
	<div class="box last">One</div>
	<div class="box">Two</div>
	<div class="box">Three</div>
</div>
```	
			
####Sticky
		
The utility class of `.sticky` can be used to anchor items to the beginning of a group.		

```html
<div class="group">
	<div class="box">One</div>
	<div class="box sticky">Two</div>
	<div class="box">Three</div>
</div>
```							
			
*elements within the same order index will then be sorted by source order.
			
			
###Reverse

The ordering of elements can be reversed with `.reverse`

```html
<div class="group reverse">
	<div class="box">One</div>
	<div class="box">Two</div>
	<div class="box">Three</div>
	<div class="box">Four</div>
</div>
```			
			
------

##Vertical

The grids main axis can be rotated 90° by adding class `.vertical` to `.group`.
				
```html
<div class="group vertical">
	<div class="box-1"></div>
	<div class="box-2"></div>
	<div class="box-3"></div>
	<div class="box-2"></div>
	<div class="box-1"></div>
	<div class="box-3"></div>	
</div>
```			
			
------

##Responsive

The following can be prefixed to all of the classes above

`small-` [0rem, 40rem]

`medium-` [40.063rem, 64rem]

`large-` [64.063rem, 99999999rem]
			
```html
<div class="group large-end medium-start medium-reverse">
	<div class="box-12 large-box-2 medium-box-4"></div>
	<div class="box-12 large-box-2 medium-box-4"></div>
	<div class="box-12 large-box-2 medium-box-4"></div>
	<div class="box-12 large-box-2 medium-box-4"></div>
</div>
```			

All the Muscle classes explained above support this responsive prefixing.
			
------

##Extendable through SASS
			
The number of segments in the grid is defined in SASS
			
`$subdivisions: 12;`
			
The gutter (padding) of `.box` along the main axis.
			
`$gutter: .5rem;`
			
Currently small, medium, and large breakpoints defined. These can be modified or added to.
			
```
$mediaqueries: (
    small: ( min : 0rem, max: 40rem ),
    medium: ( min: 40.063rem, max: 64rem ),
    large: ( min: 64.063rem, max: 99999999rem )
);
```

For example if `$mediaqueries` is modified as follows, additional class prefixes of `xlarge` and `xxlarge` become available.
			
```
$mediaqueries: (
    small: ( min : 0rem, max: 40rem ),
    medium: ( min: 40.063rem, max: 64rem ),
    large: ( min: 64.063rem, max: 90rem )
    xlarge: ( min: 90.063rem, max: 120rem )
    xxlarge: ( min: 120.063rem, max: 99999999rem )
);
```							

The default classes used are:

* Flex Container `.group`
* Flex Items `.box`
			
####In SASS
			
`$flex_item_class: "box";`
			
`$flex_container_class: "box";`