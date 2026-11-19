[README.md](https://github.com/user-attachments/files/35109680/README.md)
# Site de Kalombo II

Site statique : aucun serveur, aucune base de données. Il suffit de déposer ces fichiers sur GitHub, puis de les publier avec Render.

## Contenu du dossier

- `index.html` : toutes les pages (accueil, œuvres, recherche, carnet, projets, galerie, à propos, contact)
- `css/style.css` : l'apparence (couleurs, polices, mise en page)
- `js/data.js` : **vos données** : textes du Carnet, livres et liens, citations du jour, galerie
- `js/main.js` : le fonctionnement (navigation, filtres, citation du jour). À ne pas toucher.
- `images/` : portrait et couvertures
- `404.html` : page affichée si une adresse n'existe pas

## Où modifier quoi

| Je veux changer… | Fichier |
|---|---|
| Liens des livres (Kiosque Littéraire, Amazon, éditeur), ISBN | `js/data.js`, rubrique LIVRES |
| Ajouter un texte au Carnet | `js/data.js`, rubrique TEXTES (copiez un bloc) |
| Citations du jour | `js/data.js`, rubrique CITATIONS |
| Ajouter une photo à la galerie | mettez le fichier dans `images/`, puis ajoutez une ligne dans GALERIE |
| Liens des blogs, du podcast, des prix, du mémoire | `index.html` (cherchez `href=` ou les crochets `[ ]`) |
| E-mail, WhatsApp, Instagram, Facebook, mentions légales | `index.html`, section Contact et pied de page |
| Retirer le bandeau « Version de travail » | `index.html` : supprimez la ligne `<div class="wip">…</div>` |
| Les phrases entre crochets `[ ]` | `index.html` : remplacez ou supprimez chaque crochet une fois l'information confirmée |

Conseil : dans `data.js`, n'utilisez pas l'apostrophe droite `'` à l'intérieur d'un texte entre guillemets simples ; écrivez `’`.

## 1. Mettre le site sur GitHub

Le plus simple est de le faire **depuis un ordinateur**.

1. Décompressez le fichier `kalombo-site.zip`.
2. Sur github.com, cliquez sur **+** (en haut à droite) puis **New repository**.
3. Nom : par exemple `kalombo-site`. Choisissez Public (ou Private). Cliquez **Create repository**.
4. Sur la page du dépôt, cliquez **uploading an existing file** (ou **Add file > Upload files**).
5. Glissez **tout le contenu du dossier décompressé** (index.html, 404.html, README.md et les dossiers css, js, images) dans la fenêtre. Les dossiers doivent être déposés avec leurs fichiers.
6. Écrivez un message (ex. « Premier dépôt ») et cliquez **Commit changes**.

Depuis un téléphone : ouvrez github.com dans le navigateur en « version ordinateur ». Pour les dossiers, créez d'abord le fichier en tapant son chemin (ex. `css/style.css`), ou ouvrez le dossier voulu puis **Add file > Upload files** pour y déposer les images.

### Modifier ensuite un fichier directement sur GitHub

Ouvrez le fichier, cliquez sur le crayon, modifiez, puis **Commit changes**. Render republie le site automatiquement.

## 2. Publier avec Render

1. Créez un compte sur render.com (vous pouvez vous connecter avec GitHub).
2. Cliquez **New +** puis **Static Site**.
3. Autorisez Render à accéder à GitHub et choisissez le dépôt `kalombo-site`.
4. Remplissez :
   - **Branch** : `main`
   - **Build Command** : laissez vide (si Render exige une valeur, mettez `echo ok`)
   - **Publish Directory** : `.` (un point)
5. Cliquez **Create Static Site**. Au bout de quelques minutes, votre site est en ligne à une adresse du type `nom-du-site.onrender.com`.

Ensuite, chaque modification validée sur GitHub est publiée automatiquement.

### Nom de domaine personnel (facultatif)

Dans Render, ouvrez votre site, puis **Settings > Custom Domains**, et suivez les instructions pour ajouter votre domaine chez votre registraire. Vérifiez les conditions et tarifs actuels sur render.com.

## Ce que ce site ne fait pas encore

- Formulaire de contact (il y a seulement les liens e-mail et WhatsApp)
- Commentaires modérés (ils demandent un service externe)
- Interface d'administration (vous modifiez les fichiers sur GitHub)
- Version anglaise
- Aperçus de partage (Open Graph), plan du site (sitemap), données structurées pour Google
- Recherche sur tout le site (seule la liste des ouvrages collectifs et préfaces est filtrable)

## Avant de publier

Relisez les phrases entre crochets `[ ]`, la section « Prix et sélections » et la phrase sur les prix de la page « À propos », puis faites relire les mentions légales.
