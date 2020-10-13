### Requete non protégé des failles XSS

Nb : Attraper les erreurs SQL avec `die(print_r($db->errorInfo()));`

```php
<?php

$servname = 'localhost';
$dbname = 'test';
$user = 'root';
$password = '';

$sql = 'SELECT jeux_video.nom, jeux_video.prix FROM `jeux_video` WHERE jeux_video.possesseur = \'Florent\' ORDER BY jeux_video.prix DESC LIMIT 0, 5';


try {
    $db = new PDO("mysql:host=$servname;dbname=$dbname;charset=utf8",$user,$password);
    $db->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
    $db->beginTransaction();
    $req = $db->query($sql) or die(print_r($db->errorInfo()));
;

} catch(PDOException $e){
    $db->rollBack();
    echo "Erreur : " . $e->getMessage();
}

while($donnees = $req->fetch()){

    echo $donnees['nom'] . '<br>';
}

$req->closeCursor();
```
