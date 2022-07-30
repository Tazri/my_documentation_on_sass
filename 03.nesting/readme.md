Nesting
=======
Sass lets nest css selectors like html. Below the format :

```scss
selector {
    /* here selector property */

    sub_selector{
        /* here sub selector css property */
    }
}
```
<hr />
<br />

## Sass Nested Rules
It explain above. Here another deep example with output :

```scss
/* Nested Example in Sass */

nav {
    ul {
        margin :0px;
        padding : 0px;
        list-style: none;
    }

    li{
        display: inline-block;
    }

    a {
        display: inline-block;
        padding : 10px 15px;
        text-decoration: none;
        
        /* select the parent by using & */
        &:hover{
            color : aliceblue
        }
    }
}
```
output :
```css
/* Nested Example in Sass */
nav ul {
  margin: 0px;
  padding: 0px;
  list-style: none;
}
nav li {
  display: inline-block;
}
nav a {
  display: inline-block;
  padding: 10px 15px;
  text-decoration: none;
  /* select the parent by using & */
}
nav a:hover {
  color: aliceblue;
}

```

<hr />
<br />

## Sass Nested Properties
Many css has same prefix, like **background-color**, **background-size**, **text-align** etc. In sass can write them as nested properties. Format like : 

```scss
selector{
    prefix: {
        properties_name :value;
        properties_name :value;
        properties_name :value;
    }
}
```

**Here simple example :**
```scss
body {
    // nested properties
    font: {
        family : Recursive, cursive, arial;
        size : 20px;
        weight : bold;
    }

    background: {
        position: center;
        size: cover;
    }
}
```

output :
```css
body {
  font-family: Recursive, cursive, arial;
  font-size: 20px;
  font-weight: bold;
  background-position: center;
  background-size: cover;
}
```
<hr />
<br />

[< Variables](./../02.variables/readme.md
) | [README](./../README.md) | [@import >](./../04.import/readme.md)
---------------------------------