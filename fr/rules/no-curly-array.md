<!-- Good Practices -->
# No Curly Array

It is possible to reach specific elements of a PHP array using both square brackets `[  ]` and curly brackets `{  }`. 

```php
<?php

$x = array(1, array(2,3,4,5));

$x[1][0]; // 2
$x{1}[1]; // 3
$x[1]{2}; // 4
$x{1}{3}; // 5

?>
```
Curly brackets `{  }` are possible, but are almost never used. It is a good practice that is recommended.

## Rule Details

The following are considered a warning : 

```php
<?php

$x{1}[1]; 
$x[1]{2}; 
$x{1}{3}; 

?>
```

The following pattern are OK : 

```php
<?php

$x[1];
$object->property[0]['index'];
$x[0][1][] = 2;

?>
```

<!--
## When Not To Use It
Please, always use it.
-->

## Further Reading

* [Strings](http://php.net/strings)
* [Arrays](http://php.net/array)
