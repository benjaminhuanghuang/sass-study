- Define a mixin : @mixn
```
@mixin warning {
  background-color: orange;
  color: #fff;
}

```

- Use it in other place: @include
```
.warning-button {
  @include warning;    //use the mixin
  padding: 8px 12px;
}
```

- Mixin arguments, variable arguments, default value
```
@mixin box($radius: 6px, $border: 1px solid #000) {
  @include rounded($radius);
  border: $border;
}

@mixin box-shadow($shadows...) {
  box-shadow: $shadows;
  -moz-box-shadow: $shadows;
  -webkit-box-shadow: $shadows;
}

#header {
  @include box($border: 1px solid #fff, $radius: 12px);
  @include box-shadow(2px 0px 4px #999, 1px 1px 6px $secondary-color);
  height: $header-height;
  background-color: $theme-color;
}
```

```
@mixin rounded($radius: 6px) {
  border-radius: $radius;
}
@mixin box($radius: 6px, $border: 1px solid #000) {
  @include rounded($radius);
  border: $border;
}
```

- Pass content to mixin : @content
```
@mixin apply-to-ie6{
  * html{
    @content
  }
}

@include apply-to-ie6{
  body {
    font-size: 125%
  }
}
```