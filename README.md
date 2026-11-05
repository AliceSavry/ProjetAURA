# Le projet AURA

Escape game pédagogique créé par Alice Savry pour réviser les coûts complets en BTS GPME.

## Le scénario

La journée de cours est terminée et une soirée attend les apprenants. Mais AURA, la nouvelle intelligence artificielle de leur école, a verrouillé les portes. Pour sortir, ils doivent traverser cinq salles, résoudre quinze énigmes et réunir cinq indices pour trouver le code de désactivation.

Les salles sont la pédagogie, la salle des formateurs, la salle de pause, le service commercial et l’accueil. Une introduction cinématographique présente le contexte. Elle peut être mise en pause, lue sans animation ou passée.

## Ouvrir le jeu sur un ordinateur

Télécharger le dossier complet en conservant sa structure, puis ouvrir `index.html` dans un navigateur récent. Les décors et le jeu fonctionnent sans connexion ; le formulaire Notion nécessite Internet. Le fichier HTML autonome fourni séparément contient aussi les images et peut être distribué seul.

## Publier avec GitHub Pages

1. Créer ou ouvrir le dépôt GitHub destiné au jeu.
2. Déposer **le contenu de ce dossier à la racine du dépôt**, notamment `index.html`, `styles.css`, `game.js`, `config.js`, `.nojekyll` et le dossier `assets`. Ne pas déposer seulement l’archive ZIP.
3. Dans le dépôt, ouvrir **Settings → Pages**.
4. Dans **Build and deployment**, sélectionner **Deploy from a branch**.
5. Choisir la branche **main** et le dossier **/ (root)**, puis enregistrer.
6. Lorsque GitHub indique que le site est publié, ouvrir **Visit site** et communiquer ce lien aux apprenants.

Aucune compilation, aucun serveur applicatif et aucune clé d’API ne sont nécessaires. Les chemins des images et des fichiers sont relatifs : le jeu fonctionne aussi sous une adresse de type `https://utilisateur.github.io/projet-aura/`.

Documentation officielle : https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site

## Formulaire de fin

Après la résolution des cinq salles, un code correct ouvre le formulaire Notion dans un nouvel onglet. Le jeu affiche également un bouton pour le rouvrir et un bouton pour copier le code.

Le formulaire demande seulement **Prénom, nom** et **Code trouvé**. L’apprenant valide lui-même l’envoi dans Notion. Le jeu n’envoie pas de réponse automatiquement et ne demande pas d’adresse e-mail. Les réponses sont conservées dans la base Notion, pas dans ce dépôt.

Le lien du formulaire peut être modifié dans `config.js`, dans la propriété `formUrl`.

## Adapter le jeu

- `index.html` : structure de la page et chargement des fichiers.
- `styles.css` : présentation, adaptation au téléphone et défilement cinématographique.
- `game.js` : scénario d’introduction, questions, réponses et progression.
- `config.js` : lien du formulaire et référence du Genially d’origine.
- `assets/` : les huit nouveaux décors du centre de formation.

Le bloc `STORY` contient le texte d’introduction. Le tableau `ROOMS` contient les cinq salles, leurs questions et leurs indices. Les questions numériques acceptent notamment la virgule décimale française.

La progression est enregistrée localement dans le navigateur, sous la clé `aura-couts-complets-v1`. Le bouton **Recommencer** efface cette progression après confirmation. Une ancienne partie en cours est conservée lors de la mise à jour du jeu.

## Vérification avant diffusion

Ouvrir le site publié sur ordinateur et sur téléphone, regarder l’introduction, tester les commandes Pause et Lire sans animation, puis parcourir les salles. Vérifier que le formulaire public s’ouvre sans connexion au compte de la formatrice et permet l’envoi d’une réponse.

Les tests automatiques du parcours ne créent aucune réponse dans Notion.

## Origine des décors

Huit nouveaux décors ont été générés spécialement pour cette adaptation : école, atrium, pédagogie, salle des formateurs, pause, service commercial, accueil et sas de sortie. Les instructions de génération sont conservées dans `PROMPTS_IMAGES.md`. Ces décors remplacent les visuels du Genially dans cette version.
