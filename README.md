# TerminalOS

Maquette mobile minimaliste inspirée des contrôles de fenêtre de macOS, avec un terminal fictif.

## Commandes de démonstration

- `help` — afficher les commandes disponibles
- `clear` — effacer la sortie
- `date` — date locale
- `whoami` — utilisateur fictif
- `pwd` — chemin fictif
- `ls` — fichiers de démonstration
- `echo TEXTE` — afficher du texte
- `uname` — système fictif
- `neofetch` — résumé du système simulé
- `open-source` — afficher les références open source

Touchez l'écran noir pour ouvrir la console. Les commandes rapides permettent de tester les exemples. L'historique de session se parcourt avec les flèches haut/bas.

## Références open source

- [BusyBox](https://busybox.net/)
- [GNU Coreutils](https://www.gnu.org/software/coreutils/)
- [Toybox](https://landley.net/toybox/)

Ces projets sont présentés comme références ; aucun binaire n'est inclus ou exécuté par TerminalOS.

## Sécurité et portée

TerminalOS est une démo web autonome. Toutes les commandes sont simulées en JavaScript dans le navigateur : elles ne lancent pas de processus, ne lisent pas les fichiers du téléphone et ne modifient pas l'appareil.

## Déploiement

Le workflow GitHub Actions de Pages est dans `.github/workflows/pages.yml`. Dans **Settings → Pages**, configure la source **GitHub Actions** si nécessaire, puis vérifie l’onglet **Actions** pour confirmer le résultat du déploiement.