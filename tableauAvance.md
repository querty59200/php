* Existence d'une ___clé___ `array_key_exists`  
```php
<?php
$coordonnees = array (
    'prenom' => 'François',
    'nom' => 'Dupont');

array_key_exists('nom', $coordonnees)) // Renvoie true
?>
```
* Existence d'une ___valeur___  `in_array` ou `array_search`
```php
<?php
$fruits = array("pomme", "poire", "banane");
in_array("banane", $fruits); // Renvoie true
?>
// OU
array_search("poire", $banane); // Renvoie 2 ou false si inexistant.
```
