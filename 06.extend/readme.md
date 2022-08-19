@extend
=======
The **@extend** directive lets share a set of css properties from one selector to another selector. Like inheritance in programming langauge. Here simple format :

```scss
.selector_one {
    property : value;
}

.selector_two {
    @extend .selector_one;
}
```

**Here simple example :**
```scss
/* extend.scss file */

.botton_basic {
    padding : 20px 10px;
    border : 2px solid purple;
}

.botton_back {
    @extend .botton_basic;
    background-color: aliceblue;
}
```

output :
```css
/* extend.scss file */
.botton_basic, .botton_back {
  padding: 20px 10px;
  border: 2px solid purple;
}

.botton_back {
  background-color: aliceblue;
}
```
<hr />
<br />

[< @mixin](./../05.mixin/readme.md) | [README](./../README.md) | [Condition >](./../07.condition/readme.md)
----------------------------------------