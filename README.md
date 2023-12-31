# Notice d'utilisation Git et Github

###### Par Ahmad Daoud | Rémi Renaut | Lucas Bonnaire | Mathys Schmitter
---


Git est une solution de versioning et de collaboration, créé pour les projets logiciels mais capable de travailler sur tout fichier texte.

## Les commandes Git (en local)

```git init``` est la première commande à écrire lors de la création d'un projet. Elle sert à initialiser un projet Git dans le répertoire courant.

---

```git status``` sert à vérifier l'état du projet par rapport à ce qui est enregistré dans les versions.

---

```git log``` affiche l'historique des commits, leurs id, leurs messages et les changements effectués.

---

```git add {file}``` sert à ajouter au 'stage' - c'est à dire au versioning provisoire - les modifications effectuées sur le fichier cible. (création, modification, suppression...).

---

```git commit -m "{commentaire}"``` sert à envoyer le contenu actuel du 'stage' dans le projet. Cela crée dans le jargon Git un 'commit'. On peut visualier cela comme une 'étape' du projet.
L'argument ```--amend``` sert quant à lui à modifier le commit le plus récent en cas d'erreur par exemple.

---

```git amend -m (id du commit)``` supprime tout les commits après le commit choisi sans supprimer les changements. Cela permet de crée un seul commit organisé pour plusieurs changements, mais peut aussi être utile pour changer le message du commit.


---

#### Nettoyer l'historique :
Lorsque l'on a un problème avec un git commit, il est possible de supprimer ce commit et de revenir au commit précédent. Pour ce faire, il faut utiliser la commande :\
```git reset "id du git sur lequel on veux revenir"```

Ainsi, pour supprimer le dernier commit et nettoyer l'historique, il faut utiliser la commande précédente avec l'ID, non pas du dernier mais de l'avant dernier. De cette manière, le dernier commit est supprimé et le repository revient à l'avant dernier commit.


## Stratégies pour développer sur plusieurs branches

![représentation des branches git](git-branches-merge.png)

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

----

#### Pour fusionner (ou "merger") votre branche vers la branche principale :master:
En tant que propriétaire, on peut directement se mettre sur la branch main et faire :\
```git merge "nom de la branche"```

Par exemple, il est possible de faire ceci à partir du main:\
```git merge main```\
afin d'appliquer les changements de la branche principale sur la branche que l'on est entrain de modifier.






## Github 
### Clone un projet sur github

Pour clone un projet de github en local on peut utiliser la commande \
```git clone (lien du repository github)```


### La commande Remote 
Cette commande nous permet de mettre notre repository local en ligne sur github.
Afin d'accomplir ceci, on crée une version de notre repo sur github, ensuite on utilise la commande : \
```git remote add origin (lien du repository sur github)```


### Le fichier .gitignore
Tout les fichiers dont les noms ce trouvent dans le fichier .gitignore seront ignorés par les commandes git push et resteront en local. 


### Clone un projet sur github

Pour clone un projet de github en local on peut utiliser la commande
```git clone (lien du repository github)```

### La commande Remote 
Cette commande nous permet de mettre notre repository local en ligne sur github.
Afin d'accomplir ceci, on crée une version de notre repo sur github, ensuite on utilise la command

### Pull requests

#### Si on est un contributeur : 
Pour ajouter nos changements de branches sur github, si on est pas propriétaire du main, on fait un pull request afin de demander la mise en place du ou des changements.  
 

#### Si on est le propriétaire : 
En tant que propriétaire, on peut directement se mettre sur la branch main et faire : \
```git merge (nom de la branche)```

à partir du main afin d'appliquer les changements sur la branche principale.


### Exemples d'utilisations

Nous avons pour projet de créer un jeu Unity, j'ai donc eu la problématique de devoir syncroniser les fichier de projet Unity entre mon PC fixe et mon PC portable.

Git m'a permit de le faire, tout en ignorant les fichiers qui sont inutile à syncroniser avec le fichier .gitignore. 

Des branches pourront être créées pour segmenter les fonctionnalités à effectuer...

