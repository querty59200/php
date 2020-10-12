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

* La variable globale `$_GET` est un array associatif
```php
<?php
// bonjour.php
$_GET['nom'] // renvoie la string Dupont
?>
```

* La variable globale `$_POST` est un array associatif
```php
<?php
// bonjour.php
$_POST['nom'] // renvoie la string Dupont
?>
```
Il est nécessaire de préciser dans le formulaire les `name`

* Il est nécessaire de tester la présence des clés avec `isset()`
```php
<?php
if (isset($_GET['nom']) AND isset($_GET['prenom'])) {
	echo 'Bonjour ' . $_GET['prenom'] . ' ' . $_GET['nom'] . ' !';
} else {
	echo 'Il faut renseigner un nom et un prénom !';
} 
?>
```
* Les failles XSS
`htmlspecialchars` pour afficher les balises
`strip_tags` pour retirer les balises
