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
- lien : le numéro Steam du jeu (ex. `730` pour Counter-Strike 2, visible dans l'adresse de sa page Steam) pour afficher son image et ouvrir sa page ; sinon l'adresse du site officiel entre guillemets, ou `""` pour une simple recherche Steam
- description : une phrase courte

## Soirée LAN

La page `soiree.html` sert à choisir ensemble les jeux d'une soirée pour que chacun les installe et les mette à jour avant d'arriver. L'organisateur crée la soirée et envoie le lien ; chaque joueur entre son pseudo, coche les jeux auxquels il veut jouer (gratuits ou payants) et renvoie le lien. Les jeux choisis par au moins la moitié du groupe et jouables au nombre de joueurs forment le programme. Dans « Ma préparation », chacun coche les jeux installés et à jour, et tout le monde voit qui est prêt. Toute la soirée est stockée dans le lien, sans serveur.
