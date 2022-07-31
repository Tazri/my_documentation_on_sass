@mixin
======

**@mixin** is one kind of user define function in sass. Create a funtion with css code by using **@mixin** keyword and use this function by **@include** keyword.

## Define a mixin 
A mixin is defined with @mixin directive. Here simple format : 

```scss
@mixin mixin_name {
    property: value;
    property: value;
    /* ... */
}
```

and use the mixin by **@include**. Here : 

```scss
.selector {
    @include mixin_name;
}
```

Bud here mixin is not function in sass. In sass, **@mixin** and **@include** called directive.

**Example of using mixin :**
```scss 
/* important.scss file */
@mixin important-text {
    color : red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid blue;
}

body {
    @include important-text;
    background-color: aliceblue;
}
```

output 
```css
/* important.scss file */
body {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid blue;
  background-color: aliceblue;
}
```

<hr />
<br />

Passing Variables to a Mixin 
============================
Mixin can accept argument like a function.This way pass variable to a mixin. Here simple mixin format with **parameter** :

```scss
/* define mixin with two parameter */
@mixin mixin_name($color,$width){
    border : $width solid $color;
}

.selector_one{
    // call mixin with two vlaues
    @include mixin_name(aliceblue,2px); 
}

.selector_two{
    @include mixin_name(darkblue,5px);
}
```

**Here we can use this feature for browser vendor prefixes :**
```scss
/* paramter.scss file */
@mixin transform($property){
    -webkit-transform: $property;
    -ms-transform: $property;
    transform: $property;
}

.my_box{
    @include transform(rotate(20deg) translate(20px,10px));
}
```

output :
```css
/* paramter.scss file */
.my_box {
  -webkit-transform: rotate(20deg) translate(20px, 10px);
  -ms-transform: rotate(20deg) translate(20px, 10px);
  transform: rotate(20deg) translate(20px, 10px);
}
```

## Default Values of Mixin
In sass, it is possible to define a default vlaue for mixin variable. Format is :

```scss
@mixin mixin_name($one : default_value,$two : default_value){
    property_one : $one;
    property_two : $two;
}

.selector {
    @include mixin_name;
}

.selector_two{
    @include mixin_name(value,value);
}
```

**Here example of default values format of mixin :**

```scss
/* default_value */

@mixin important($color : aliceblue){
    border : 4px solid $color;
}

.container{
    @include important;
}

.p{
    @include important(darkblue);
}
```

output : 
```css
/* default_value */
.container {
  border: 4px solid aliceblue;
}

.p {
  border: 4px solid darkblue;
}
```

<hr />
<br />

[< @import](./../04.import/readme.md) | [README](./../README.md) | [@extend >](./../06.extend/readme.md)
----------------------------