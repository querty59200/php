* Les variables : `string` `int` `float` `bool` `NULL`
* `$ageDuVisiteur = 12;`
* Concatenation : `echo "il a $ageDuVisiteur aujourd'hui"` OU `echo 'il a ' . $ageDuVisiteur . ' aujourd'hui'`
* Condition if elseif else : 
```php
<?php

$autorisation_entrer = "Oui";

if ($autorisation_entrer == "Oui")
{
    // instructions à exécuter quand on est autorisé à entrer
}
elseif ($autorisation_entrer == "Non")
{
    // instructions à exécuter quand on n'est pas autorisé à entrer
}
else
{
    echo "Euh, je ne connais pas ton âge, tu peux me le rappeler s'il te plaît ?";
}
?>
```
* Condition switch
```php
<?php
$note = 10;

switch ($note)
{ 
    case 0: 
        echo "Tu es vraiment un gros nul !!!";
    break; 
    case 10: // etc. etc.
        echo "Tu as pile poil la moyenne, c'est un peu juste…";
    break;   
    case 20:
        echo "Excellent travail, c'est parfait !";
    break;
    default:
        echo "Désolé, je n'ai pas de message à afficher pour cette note";
}
?>
```
* Condition ternaire :
```php
<?php
$age = 24;
$majeur = ($age >= 18) ? true : false;
?>
```
Boucle while :
```php
<?php
while ($continuer_boucle == true)
{
    // instructions à exécuter dans la boucle
}
?>
```
* Condition for :
```php
<?php
for ($nombre_de_lignes = 1; $nombre_de_lignes <= 100; $nombre_de_lignes++)
{
    echo 'Ceci est la ligne n°' . $nombre_de_lignes . '<br />';
}
?>
```
### Les NameSpaces `namespace A;`
