Les fonctions natives
* `strlen()`
* `str_replace('b', 'p', 'babar')` // Renvoie papar 
* `str_shuffle('abcde')` // Renvoie bdcae par exemple
* `strtolower('ABCD')` // Renvoie abcd
* `strtoupper('wxyz')` // Renvoie WXYZ
* `date('Y')` // Renvoie 2020

* Les fonctions non natives
```php
<?php

function volumeCone(float $rayon, float $hauteur) : float
{
return $rayon * $rayon * 3.14 * $hauteur * (1/3);
}

$volume = volumeCone(1.2, 3.4);

echo 'le volume est de ' . $volume . ' cm3';

?>
```
