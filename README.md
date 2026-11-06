# Ta journée, sans les immigrés

Simulateur en une seule page (HTML, CSS et JavaScript, sans dépendance ni serveur). Le visiteur retire les immigrés et voit, métier par métier, quelle part des emplois de sa journée est concernée.

## Principe

- Chaque carte montre la part d'immigrés parmi les personnes en emploi dans un métier, avec la source et l'année.
- Hypothèse affichée sur la page : **aucun poste n'est repris**. Dans la réalité, des postes seraient repris, d'autres non. Aucune source publique ne permet de dire lesquels.
- Deux profils : Île-de-France (chiffres du recensement 2018) ou moyenne nationale (recensement 2017).
- Aucune donnée personnelle n'est collectée : pas de cookie, pas de statistique, pas de requête vers un serveur, hors les polices Google Fonts.

## Données

Toutes les valeurs sont écrites dans le tableau `CARDS` de `index.html`. La liste complète des chiffres, avec le document et le tableau d'origine, est dans [SOURCES.md](SOURCES.md).

Définition utilisée (Insee) : un immigré est une personne née étrangère à l'étranger et résidant en France. Il peut être devenu français.

## Limites connues

- Les chiffres par métier datent de 2017 (France) et 2018 (Île-de-France).
- Ils concernent tous les immigrés, étrangers et naturalisés confondus.
- Les 2e et 3e générations ne sont pas traitées : aucune part par métier n'est publiée.
- Les personnes en situation irrégulière ne sont pas traitées : aucune source officielle ne les compte.
- Hors Île-de-France, seule la moyenne nationale est disponible.
- Les métiers sont ceux des 87 familles professionnelles de l'Insee. Par exemple, « conducteurs de véhicules » n'isole ni les VTC ni les livreurs.
- Le CEPII ne donne qu'une fourchette commune « 12 à 13 % » pour les éboueurs, caissiers et vendeurs réunis.

## Publier avec GitHub Pages

1. Créer un dépôt public et y envoyer ces fichiers à la racine.
2. Dans le dépôt : **Settings > Pages**, source **Deploy from a branch**, branche `main`, dossier `/ (root)`.
3. Le site est publié à l'adresse `https://<compte>.github.io/<dépôt>/`.
4. Pour un nom de domaine propre : ajouter un fichier `CNAME` contenant uniquement le nom de domaine, puis créer chez le bureau d'enregistrement un enregistrement `CNAME` vers `<compte>.github.io` (ou les enregistrements `A` indiqués par la documentation GitHub Pages pour le domaine racine). Activer ensuite **Enforce HTTPS**.

## Rester anonyme

- Utiliser un compte GitHub dédié, sans lien avec une identité personnelle.
- Configurer git avec un nom neutre et l'adresse « noreply » du compte, avant le premier commit : `git config user.name "..."` et `git config user.email "<id>+<compte>@users.noreply.github.com"`.
- Activer **Block command line pushes that expose my email** dans les réglages d'adresse e-mail du compte.
- Chez le bureau d'enregistrement du domaine, activer la protection des données WHOIS et utiliser une adresse e-mail dédiée.
- Ne pas mettre de nom, d'adresse ou de lien personnel dans ce dépôt (README, commits, issues).

## Licence

À choisir avant la publication. Les données reprises viennent de publications publiques de l'Insee, de la Dares et du CEPII.
