# Notice d'utilisation Git et Github

Git est une solution de versioning et de collaboration, créé pour les projets logiciels mais capable de travailler sur tout fichier texte.

## Les commandes Git (en local)

```git init``` est la première commande à écrire lors de la création d'un projet. Elle sert à initialiser un projet Git dans le répertoire courant.

```git status``` sert à vérifier l'état du projet par rapport à ce qui est enregistré dans les versions.

```git add {file}``` sert à ajouter au 'stage' - c'est à dire au versioning provisoire - les modifications effectuées sur le fichier cible. (création, modification, suppression...).

```git commit -m "{commentaire}"``` sert à envoyer le contenu actuel du 'stage' dans le projet. Cela crée dans le jargon Git un 'commit'. On peut visualier cela comme une 'étape' du projet.


## Stratégies pour développer sur plusieurs branches

#### Pour créer une branche:
```git checkout -b "nom de la branche"```


Cette commande va directement créer une branche et basculer le git sur celle-ci. Ainsi, plus besoin d'utiliser de commande pour basculer sur cette branche.

----

#### Pour basculer sur une autre branche:
```git checkout "nom de la branche"```

Cette commande permet de changer de branche mais il arrive parfois de ne plus avoir en tête les noms des branches. Dans ce cas il est possible de...

----

#### Visualiser le nom des branches:
```git branch```

Comme introduit précédemment, cette commande permet de lister vos branches qui ont été "push"

#### Pour fusionner (ou "merger") votre branche vers la branche principale :master:


## Github 

### Pull requests

#### Si on est un contributeur : 
Pour ajouter nos changements de branches sur github, si on est pas propriétaire du main, on fait un pull request afin de demander la mise en place du ou des changements.   

#### Si on est le propriétaire : 
En tant que propriétaire, on peut directement se mettre sur la branch main et faire :
```git merge (nom de la branche)```

à partir du main afin d'appliquer les changements sur la branche principale.

