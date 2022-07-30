@import
========
Sass can keeps the css code **DRY (DON'T REPEAT YOURSELF)** by using **@import**. In that case create small sass files and include all file in main folder by using **@import** keyword. Here syntax : 

```scss
@import "filename_one";
@import "filename_two";
@import "filename_three";
```
**Note : Not necessary to specify extention when import sass file, sass automatically assumes that it sass file.**

**Example :**
```scss
/* color.scss file */

$text_color : aliceblue;
$bg_color : darkblue;
```

```scss
/* body.scss file */

@import './color';

body {
    background-color: $bg_color;
}
```

```scss
/* main.scss file */
@import './body';

.container{
    color : $text_color;
}
```
output :
```css
/* main.scss file */ /* body.scss file */ /* color.scss file */
body {
  background-color: darkblue;
}

.container {
  color: aliceblue;
}
```

<hr />
<br />

## Sass Partials
By default, sas transpiles all the file directly. If want to import a file, but do not need to file transpiled directly then use **sass partials** syntax. In that case filename start with **underscore ( _ )**. Here the example : 

```scss
@import '_partial_filename';

// not necessary to write underscore from start
// sass do this by default
@import 'partial_filename'; 
```

**Another example :**
```scss
/* it is _color.scss */
$text_color : aliceblue;
$bg_color : darkblue;
```

```scss
/* another_main.scss file */

// import partial file
@import './partials/color'; // not necessary to write underscore for import file

body{
    background-color: $bg_color;
    color : $text_color;
}
```
output : 
```css
/* another_main.scss file */ /* it is _color.scss */
body {
  background-color: darkblue;
  color: aliceblue;
}

```

<hr />
<br />

[< Nesting](./../03.nesting/readme.md) | [README](./../README.md) | [@mixin >](./../05.mixin/readme.md)
------------------------------------------------