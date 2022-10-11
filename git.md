## Configuration GIT
- git config --global user.name "mon nom"
- git config --global user.email "mon email"

- git config --list

## Initialisation dépôt git
- git init

## Verification de l'état de la working copy
- git status 

## Ajout d'un fichier dans le staging area ( index )
- git add <NomDuFichier ou Nom Du Dossier>
## Raccourcis pour ajouter tout les fichiers d'un coup dans l'index
- git add .

## Voir les modifications
- git diff

## Sauvegarder l'état
- git commit -m "Titre du commit" -m "Description du commit"
## Ajouter tout les fichier dans l'index et les commits
- git commit -am "Titre du commit" -m "Description du commit"

## Supprimer un fichier ou un dossier
- rm <NomDuFichier>
- git add <NomDuFichier>
### ou
- git rm <NomDuFichier>  = à rm + git add

## Visualiser l'historique
- git log
- git log --oneline  <!--Voir l'historique sur une ligne  -->
### Option
- on peux rajouter -2 pour voir que les 2 derniers commits
- --graph <!-- Permet de voir un petit schema des branches -->

## Visualiser l'historique d'un fichier
- git blame  <!-- Inspecte le fichier pour voir qui a commit a qu'elle ligne -->
- git blame -L 1,2 <NomDuFichier> <!-- Inspecte entre les lignes 1 et 2  du fichier -->

## Deplacer le Head sur un commit anterieur
- git checkout <numeroDuCommit>

## remettre un fichier dans l'état du dernier commit connue 
- git checkout -- <NomDuFichier>

## Restauration d'une ancienne version
- git checkout <NumeroDeCommit> -- <NomDuFichier>

## Supprimé les fichier non suivie
- git clean -f

## Annuler les changements d'un commit
- git revert <NumeroDuCommit>
### option
--no-edit <!--permet de ne pas avoir a modifier le commit -->
--no-commit <!--Fait le revert sans rajouter de commit -->

## Annuler des modification
- git reset <!-- desindexé des fichiers -->
- git reset --soft <numeroDeCommit> <!-- Permet de déplacer la branche sur laquel pointe le HEAD sans rien faire d'autre -->
- git reset <numeroDeCommit> <!-- Permet de deplacer le HEAD et la brache et desindexe les fichier, mais garde les modification ->
- git reset --hard <numeroDeCommit> <!-- Permet de revenir a un etat antérieur -->

## Création de branche
- git branch <nomDeLaNouvelleBranche>
- git checkout <nomDeLaNouvelleBranche> <!-- switcher sur la nouvelle branche -->
### ou
- git checkout -b <nomDeLaNouvelleBranche> <!-- Créé la branche et switch dessus>

## Afficher la liste des branches
- git branch --list

## Effacer branche
- git branch -d <NomDeLaBranche> <!-- Effacera la branche seulement si elle a été fusionner -->
- git branch -D <NomDeLaBranche> <!-- Effacera la branche même si elle a pas ete fusionner>

## Fusion des branches
- git merge <NomBrancheprincipal> <NomDeBrancheAFusionner>
### Liste des branches merge
- git branch --merged
### Liste des branches non merge
- git branch --no-merged

## Faire une sauvegarde de fichier non commiter pour aller travailler sur une autre branche
- git stash
- git stash -u <!-- si on a des fichier non suivie -->
### pour utiliser la sauvegarde
- git stash apply <!-- apllique la sauvegarde et la garde en mémoire -->
- git stash pop <!-- applique les changement et la supprime -->

## Rectifier le dernier commit
- git commit --amend

## Fusionner deux branches sans commit de merge
- git rebase <NomDeBranche>

## recupération de version perdu
- git reflog
-- on récupere le commit que l'on veut récupérer
- git branch <NomDeBranche> <numéroDuCommitRecuperer>
- git merge <NomDeBranche>

## Création d'un tag
- git tag <nomDuTag> <!-- tag leger -->
- git tag -a <nomDuTag> -m <descriptionDuTag> <!-- Tag annoté -->

## Pour cloner un projet via un dépôt distant ( GitHub, GitLab ...)
- git clone <Lien du dépôt>

## Envoyer du code sur un dépot distant
- git push -u origin <nomDeBranch>
-- -u = Pour definir de faire un lien entre la branche et la branche du dépot distant
-- origin = dépôt distant

## Récupérer le code distant
- git fetch
- git merge 
### ou
- git pull






