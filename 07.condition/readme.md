Condition
=========
It possible to apply condition in sass like what do to in programming language with condition. In that case use **@if**, **@else if** and **else** directive. Here simple format :

```scss
@mixin mixin_name(item){
    @if (<expression>){
        /* property gose here */
    }
    @else if (<expression>){
        /* property gose here */
    }
    @else{
        /* property gose here */    
    }
}
```

**Simple example of condition :**
```scss
/* condition */
$border : 2px solid purple;

@mixin border($direction){
    /* condition appling */
    @if ($direction == up) {
        border-top : $border; 
    }@else if($direction == left){
        border-left: $border;
    }@else if($direction == right){
        border-right : $border;
    }@else{
        border-bottom: $border;
    }
}

.left_button{
    @include border(left);
}

.right_button{
    @include border(right);
}

.up_button{
    @include border(up);
}

.down_button{
    @include border(down)
}
```
ouput : 
```css
/* condition */
.left_button {
  /* condition appling */
  border-left: 2px solid purple;
}

.right_button {
  /* condition appling */
  border-right: 2px solid purple;
}

.up_button {
  /* condition appling */
  border-top: 2px solid purple;
}

.down_button {
  /* condition appling */
  border-bottom: 2px solid purple;
}
```

<hr />
<br />

[< @extend](./../06.extend/readme.md) | [README](./../README.md) | [Loop >](./../08.loop/)
-----------------------