# Carnet-EDN

## Générateur de QR code (`generateur-qr/`)

Petite application web pour créer un QR code personnalisé qui renvoie vers un lien
(portfolio sur Google Drive, site, LinkedIn…), à insérer dans un CV.

- Couleurs des points, des coins et du fond, dégradé, fond transparent, palettes prêtes à l'emploi
- Forme des points (carrés, ronds, arrondis, élégants…) et des coins
- Logo ou photo au centre (facultatif)
- Export PNG (512 à 2048 px) ou SVG (vectoriel)
- Alerte si le contraste ou les réglages risquent de rendre le code illisible

Tout se passe dans le navigateur : aucun lien ni image n'est envoyé sur un serveur.

### Utilisation

Ouvrir `generateur-qr/index.html` dans un navigateur (double-clic suffit), ou l'activer
en ligne avec GitHub Pages (Settings → Pages → branche `main`, dossier `/root`), puis
aller sur `https://<utilisateur>.github.io/Carnet-EDN/generateur-qr/`.

Bibliothèque utilisée : [qr-code-styling](https://github.com/kozakdenys/qr-code-styling) (licence MIT),
copiée dans `generateur-qr/vendor/` pour fonctionner hors ligne.
