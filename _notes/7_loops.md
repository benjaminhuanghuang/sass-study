## while
```
$j: 8;
@while $j >= 2 {
  .picture-#{$j} {
    width: $j * 10%;
  }
  $j: $j - 2;
}
```