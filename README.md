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
