# Carnet-EDN

## Générateur de QR code (`generateur-qrcode/`)

Petite application web pour créer un QR code personnalisé qui renvoie vers un lien
(portfolio sur Google Drive, site, LinkedIn…), à insérer dans un CV.

- Couleurs des points, des coins et du fond, dégradé, fond transparent, palettes prêtes à l'emploi
- Forme des points (carrés, ronds, arrondis, élégants…) et des coins
- Logo ou photo au centre (facultatif)
- Export PNG (512 à 2048 px) ou SVG (vectoriel)
- Alerte si le contraste ou les réglages risquent de rendre le code illisible

Tout se passe dans le navigateur : aucun lien ni image n'est envoyé sur un serveur.

### Utilisation

Ouvrir `generateur-qrcode/index.html` dans un navigateur (double-clic suffit), ou l'activer
en ligne avec GitHub Pages (Settings → Pages → branche `main`, dossier `/root`), puis
aller sur `https://<utilisateur>.github.io/Carnet-EDN/generateur-qrcode/`.

Bibliothèque utilisée : [qr-code-styling](https://github.com/kozakdenys/qr-code-styling) (licence MIT),
copiée dans `generateur-qrcode/vendor/` pour fonctionner hors ligne.

### Application Android

`generateur-qrcode/QR-Code-CV.apk` : la même application, installable sur Android 10 ou plus,
qui fonctionne sans internet. Les PNG sont enregistrés dans la galerie (Images › QR codes),
les SVG dans Téléchargements › QR codes, et un bouton « Partager » envoie le QR code par mail,
WhatsApp, Drive…

Installation : ouvrir le fichier .apk sur le téléphone et autoriser l'installation
d'« applications de sources inconnues » quand Android le demande.

Code source dans `generateur-qrcode/android/` (WebView native, sans dépendance). Construction :
`ANDROID_HOME=… gradle assembleRelease` depuis ce dossier ; la page `index.html` est copiée
automatiquement dans l'APK.
