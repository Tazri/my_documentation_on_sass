Variables
=========

Variable use for store a value for re-use later like in programming language. Here simple syntax to create variable in sass :

```scss
$variable_name : value;
```
**Note : underscore ( _ ) and ( - ) are same in sass.**

Type of information store in variable in sass :
- strings
- numbers
- colors
- booleans
- lists
- nulls

**Example using variable :**
```scss
$my_font : recursive, arial;
$my_color : aliceblue;
$my_font_size : 18px;
$my_with : 680px;

body {
    font-family: $my_font;
    font-size: $my_font_size;
    color: $my_color;
}

.container{
    width: $my_with;
}
```

output :
```css
body {
  font-family: recursive, arial;
  font-size: 18px;
  color: aliceblue;
}

.container {
  width: 680px;
}
```
<hr />
<br />

## Sass Variable Scope
Sass variable access only available at the level of nesting where they are defined. Example :

```scss
// gobal variable available everywhere but local variable only available only their local scope
$global_variable : value;

h1{
    $local_variable : value;
}

p{
    // here dose not available $local_variable which is define in h1.
}
```

## !global
**!global** use for define a variable as a global at anywhere. Example : 

```scss 
$my_color : aliceblue;

h1{
    $my_color: darkblue !global;
    color : $my_color;
}

p {
    color : $my_color;
}
```

output : 
```css
h1 {
  color: darkblue;
}

p {
  color: darkblue;
}
```

<hr />
<br />

[< Installation](./../01.installation/readme.md) | [README](./../README.md) | [Nesting >](./../03.nesting/readme.md)
--------------------------------------------------------