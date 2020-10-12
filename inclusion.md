* Une inclusion
```php
<?php 
include("navbar.php"); 
?>
```
* Communiquer via l'U.R.L (Uniform Resource Locator)
```php
// index.php
<?php
<a href="bonjour.php?nom=Dupont&amp;prenom=Jean">Dis-moi bonjour !</a>
?>
```

la variable globale `$_GET` est un array associatif
```php
<?php
// bonjour.php
$_GET['nom'] // renvoie la string Dupont
?>
```
