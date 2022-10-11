- Création d'une branche main.

- Création une branche developp
- De développe on creer les branche Feature

- Si un problème est détecté sur main, une branche hotfix es créée à partir de main.

- Quand le fix est terminé, on le merge sur main est developp.

- Quand un feature est finie, elle est mergée sur la branche developp

- Une branche release est créée à partir de develop

- Si fix a faire sur release, on le corrige directement sur release

- Une fois release terminé, on merge release sur main et develop

## Nom des branches

Une branche prend le nom de la fonctionnalité de la branche + la fonctionnalité traité.

### Fonctionnalité de la branche
- main
- hotfix + n°version
- develop + n°version
- Feature

ex: hotfix_v0.2 ou feature_auth

## conventionnal commit

ex: git commit -m "docs: Authentification" -m "djisdfofhsofhe"

### type de commits
- feat: Ajoute une nouvelle fonctionnalité
- fix : Corige un bug
- refractor : réécrire ou restructure du code sans changer le comportement
- style : style, supression espace blanc, etc
- docs : ajout de documentation
- test : ajout de test
- build : pipeline, dépendances, version  etc
- chore : divers commit ex: .gigtignore
