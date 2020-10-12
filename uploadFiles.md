* Via un formulaire, uploader un fichier, une image, etc...
```php
<?php
// index.php
<form action="cible_envoi.php" method="post" enctype="multipart/form-data">
        <p>
                Formulaire d'envoi de fichier :<br />
                <input type="file" name="monfichier" /><br />
                <input type="submit" value="Envoyer le fichier" />
        </p>
</form>

// cible_envoi.php
$_FILES['monfichier'] // La variable globale contient toutes les informations sur tous les fichiers uploadés

```
