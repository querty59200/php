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
<?php
if (isset($_FILES['monfichier']) AND $_FILES['monfichier']['error'] == 0)
{
        if ($_FILES['monfichier']['size'] <= 1000000)
        {
                // Testons si l'extension est autorisée
                $infosfichier = pathinfo($_FILES['monfichier']['name']);
                $extension_upload = $infosfichier['extension'];
                $extensions_autorisees = array('jpg', 'jpeg', 'gif', 'png', 'pdf');
                if (in_array($extension_upload, $extensions_autorisees))
                {
                     // On peut valider le fichier et le stocker définitivement
                     move_uploaded_file($_FILES['monfichier']['tmp_name'], 'download/' . basename($_FILES['monfichier']['name']));
                     echo "L'envoi a bien été effectué !";
                }
        }
}

```
