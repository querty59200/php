* Creation d'un tableau numéroté
```php
<?php
$prenoms = array("jean","paul","henri"); 
// OU
$prenoms[0] = "jean";
$prenoms[1] = "paul";
$prenoms[2] = "henri";
// OU
$prenoms[] = "jean";
$prenoms[] = "paul";
$prenoms[] = "henri";
```
* Affichage d'un élément du tableau numéroté
```php
<?php
echo $prenoms[1];
?>
```
* Parcours d'un tableau numéroté
```php
<?php
for($i = 0; $i < sizeof($prenoms)-1; $i++)
{
echo $prenom[$i];
}
// OU
foreach($prenoms as $prenom)
{
    echo $prenom
}
?>
```
* Creation d'un tableau associatif
```php
<?php
$coordonnees['prenom'] = 'François';
$coordonnees['nom'] = 'Dupont';
$coordonnees['adresse'] = '3 Rue du Paradis';
$coordonnees['ville'] = 'Marseille';
?>
```
* Affichage d'élément du tableau associatif
```php
<?php
echo $coordonnees['prenom'];
?>
```
* Parcours d'un tableau associatif
```php
<?php
foreach($coordonnees as $key => $value)
{
    echo $key . 'et ' . $value;
}
```
