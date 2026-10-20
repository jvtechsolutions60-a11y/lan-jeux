# LAN & Jeux

Catalogue de jeux multijoueurs pour les LAN. On choisit le nombre de joueurs et le type de jeu, et le site affiche les jeux qui correspondent (gratuits ou payants).

Site : https://jvtechsolutions60-a11y.github.io/lan-jeux/

## Ajouter ou corriger un jeu

Tout est dans `games.js`, une ligne par jeu :

```js
["Nom du jeu", joueurs_min, joueurs_max, "types", gratuit, "modes", lien, "description"],
```

- types : `tir strategie course party coop combat survie sport rpg plateforme horreur societe moba` (plusieurs séparés par un espace)
- gratuit : `1` gratuit, `0` payant
- modes : `l` réseau local (LAN), `e` même écran, `o` internet requis
- lien : le numéro Steam du jeu (ex. `730` pour Counter-Strike 2, visible dans l'adresse de sa page Steam) pour afficher son image et ouvrir sa page ; sinon l'adresse du site officiel entre guillemets, ou `""` pour une simple recherche Steam ; ou `[numéro Steam, "adresse"]` pour garder l'image Steam mais ouvrir une autre boutique (ex. Rocket League sur Epic)
- autres boutiques : la boutique principale est déduite du lien ; pour indiquer qu'un jeu est aussi sur Epic, GOG, Battle.net, EA app, Ubisoft ou Xbox, ajoutez son nom dans la liste `AUSSI` en bas de `games.js`
- description : une phrase courte

## Soirée LAN

La page `soiree.html` sert à choisir ensemble les jeux d'une soirée pour que chacun les installe et les mette à jour avant d'arriver. L'organisateur crée la soirée et envoie le lien ; chaque joueur entre son pseudo, coche les jeux auxquels il veut jouer (gratuits ou payants) et renvoie le lien. Les jeux choisis par au moins la moitié du groupe et jouables au nombre de joueurs forment le programme. Dans « Ma préparation », chacun coche les jeux installés et à jour, et tout le monde voit qui est prêt. Toute la soirée est stockée dans le lien, sans serveur.

## Versions

- **2.3** (20/10/2026) : Gratuit / Payant passe en filtre principal (à côté du nombre de joueurs, visible aussi sur mobile), petits logos des boutiques sur les filtres, les jeux et l'onglet Préparer
- **2.2** (19/10/2026) : filtre Boutique (Steam, Epic, GOG, Battle.net, EA app, Ubisoft, Xbox, Riot, navigateur), 394 jeux
- **2.1** (17/10/2026) : ergonomie et design revus, aperçu des liens partagés, favicon, lien de signalement, catalogue allégé (388 jeux)
- **2.0** (17/10/2026) : mode Soirée LAN (choisir, programme, préparer), sans serveur
- **1.1** (16/10/2026) : recherche, tri, jeu au hasard, images Steam, descriptions, 396 jeux
- **1.0** (16/10/2026) : premier catalogue (149 jeux) avec filtres joueurs, type, prix, connexion
