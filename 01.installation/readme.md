# Installation

There are serveral ways to install sass in system. below command to install sass in system by using **npm** package manager :

```bash
$ sudo npm i -g sass 
```

## How to use sass
How to compile sass file is given below :

```bash
$ sass file_name_with_path compile_file_name_with_path
```

**Here simple sass code, file name sass/simple.scss :**
```scss
/* This is simple sass file */
$textcolor : red;
$textsize : 30px;

body{
    color : $textsize;
    font-size: $textcolor;

    div{
        width : 300px;
        height : 100px
    }
}
```

**compile command compile sass file to css :**
```bash
$sass ./sass/simple.scss ./style/style.css
```
or
```bash
$sass ./sass/simple.scss:./style/style.css
```

**compiled css file ./style/style.css :**
```css
/* This is simple sass file */
body {
  color: 30px;
  font-size: red;
}
body div {
  width: 300px;
  height: 100px;
}

/*# sourceMappingURL=style.css.map */
```

<hr />
<br />

## Necessary Command
If compile the scss or sass file then use this command format : 

```bash
$ sass <input_filename_with_path>:<output_filename_with_path>
```
or
```bash
$ sass <input_filename_with_path> <output_filename_with_path>
```

If compile a file of folder sass file then use this command :
```bash
$ sass <input folder path>:<output folder path>
```

Every time compile the sass file, it create a **.css.map** file by default. If can not give the output file name with path then **sass compiler** create **css** file current folder with sass file name by default.

## Necessary Flag 

| Flag            | Use                         |
|-----------------|-----------------------------|
| --watch         | watching sass file          |
| --no-source-map | don't create .css.map file  |
| --style         | expanded or compressed file, it has to value, use like **\-\-style=expanded** and **\-\-style=compressed**. Here expanded is by default value |
| 

## Example of SCSS and SASS 
Here example of SCSS file :
```scss
/* This is simple scss file */
$textcolor  : aliceblue;
$textsize  : 30px;

body{
    color : $textcolor;
    background : $textsize;
}
```


Here example of SASS file :
```sass
/* This is simple sass file */
$textcolor  : aliceblue
$textsize  : 30px

body
    color : $textcolor
    background : $textsize
```

## Comment in Sass 
Example of comment in sass :
```scss
// single line comment
/*
    multiline comment
*/
```
<hr />
<br />

[< Go Back](./../README.md) | [Variable >](./../02.variables/readme.md)
-----------------------------------------------------------------------