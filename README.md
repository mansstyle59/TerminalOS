# TerminalOS

Maquette web mobile minimaliste inspirée des contrôles de fenêtre de macOS, avec une console de démonstration en JavaScript.

## Lancer la démo

Ouvrir `index.html` dans un navigateur ou publier le dépôt avec GitHub Pages. Touchez l'écran noir pour ouvrir le terminal.

## Commandes simulées

- `help`, `man commande` — aide générale et quelques pages de manuel
- `clear`, `date`, `whoami`, `id`, `pwd`, `uname`, `neofetch`
- `cd`, `ls [-la]`, `tree`, `find` — navigation dans une arborescence virtuelle
- `cat`, `head`, `tail`, `wc`, `grep` — lecture et recherche dans les fichiers de démonstration
- `touch`, `mkdir`, `rm [-r]` — modifications du système de fichiers virtuel
- `echo`, `printf`, `env`, `export NOM=valeur`, `history`, `true`, `false`
- `open-source` — affiche des projets open source à titre de référence

Les guillemets simples/doubles et l'échappement de base sont pris en charge pour découper les arguments. La navigation dans l'historique fonctionne avec les flèches haut/bas. Le système de fichiers et les variables exportées sont gardés en mémoire pendant la session de la page.

## Mini-jeu CyberLab

Ouvrez `hacking-game.html` pour jouer à un puzzle de déduction de code (4 chiffres distincts), avec tentatives limitées, indices, niveaux et journal de mission. Le jeu fonctionne localement dans le navigateur : aucune connexion réseau, aucune cible réelle et aucune commande de piratage n'est exécutée.

## Limites importantes

TerminalOS reste une **simulation JavaScript**, pas un shell Unix/POSIX. Les commandes sont des implémentations pédagogiques et partielles :
- aucun processus, programme ou binaire natif n'est lancé ;
- aucune lecture/écriture des fichiers réels du téléphone, de l'ordinateur ou du serveur ;
- les fichiers et dossiers sont fictifs, volatils et réinitialisés au rechargement ;
- pas de pipes (`|`), redirections (`>`), substitutions, scripts shell, permissions réelles, liens symboliques, globbing complet ou codes de sortie compatibles POSIX ;
- les options ne sont implémentées que lorsqu'elles sont explicitement prévues ; les résultats peuvent différer d'un vrai Unix ;
- `grep` utilise les expressions régulières JavaScript, et non toutes les règles de GNU grep ;
- cette démo n'est pas destinée à exécuter du code non fiable ni à remplacer un terminal système.

## Références open source

- [BusyBox](https://busybox.net/)
- [GNU Coreutils](https://www.gnu.org/software/coreutils/)
- [Toybox](https://landley.net/toybox/)

Ces projets sont **des références uniquement** : leur code et leurs binaires ne sont pas intégrés à TerminalOS.

## Déploiement

Le workflow GitHub Actions de Pages se trouve dans `.github/workflows/pages.yml`. Dans **Settings → Pages**, choisissez **GitHub Actions** comme source si nécessaire, puis vérifiez l'onglet **Actions** pour confirmer le déploiement.
