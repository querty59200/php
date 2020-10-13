### Avec des marqueurs nominatifs (possesseur = :possesseur, prix = :prix, ...)
```php
<?php

$servname = 'localhost';
$dbname = 'test';
$user = 'root';
$password = '';

$sql = 'SELECT jeux_video.nom, jeux_video.prix FROM `jeux_video` WHERE jeux_video.possesseur = :possesseur ORDER BY jeux_video.prix DESC LIMIT 0, 5';


try {
    $db = new PDO("mysql:host=$servname;dbname=$dbname;charset=utf8",$user,$password);
    $db->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
    $db->beginTransaction();
    $req = $db->prepare($sql);
    $req->execute(array('possesseur' => 'Florent'));

} catch(PDOException $e){
    $db->rollBack();
    echo "Erreur : " . $e->getMessage();
}

while($donnees = $req->fetch()){

    echo $donnees['nom'] . '<br>';
}

$req->closeCursor();
```
