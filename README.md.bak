
Gitflow en quelques mots
Gitflow sépare sur des branches isolées le code en cours de développement et le code validé et testé. Pour cela, il s’appuie sur la création de plusieurs branches dont le cycle de vie est bien défini. Voici une table contenant leurs noms, leurs cycles de vie et leurs fonctions :

| Branche	| Nombre	| Branche d’origine	| Durée de vie	| Fonction
| ------------- | ------------- | ------------- | ------------- | -------------
| master	| Unique	|					|Permanente		| Code stable, testé et validé potentiellement éligible pour une MEP (Mise En Production)
| feature	| Plusieurs	|develop			|Développement d’une feature	| Code en cours de développement qui implémente une fonctionnalité à embarquer dans la prochaine version de l’application
| develop	| Unique		| master			|Permanente		| Code de la prochaine version de l’application. Une fois que le développement d’une fonctionnalité (feature)est fini, le code est fusionné sur cette branche
| release	| Unique	| develop	| Recette	| Branche sur laquelle on corrigera les bugs détectés pendant la phase de recette
| hotfix	| Aucune/Plusieurs	|master	| Correction d’un bug	| Branche où on fait les corrections des bugs sur le code présent sur la branche master (production)

# Fonctionnalités/Features

Développe des nouvelles fonctionnalités pour la prochaine version
Existe en général uniquement dans les dépôts des développeurs


## Initialisation


Commencez à utiliser git-flow en l'initialisant dans un dépôt git existant :

 `$ git flow init `


## Commencer une feature


Le développement d'une fonctionnalité commence à partir de la branche 'develop'

Commencer le développement d'une nouvelle fonctionnalité avec :

 `$ git flow feature start MYFEATURE`

Cette commande crée une nouvelle branche de fonctionnalité basée sur 'develop' et passe sur cette branche

![alt text](http://url/to/images/feature.png)

## Terminer une fonctionnalité



Termine le développement d'une fonctionnalité. Cette action effectue les opérations suivantes:

- Fusionne MYFEATURE dans 'develop'
- Supprime la branche de fonctionnalité
- Passe sur la branche 'develop'

 `$ git flow feature finish MYFEATURE`
 
![alt text](http://url/to/images/finish-feature.png)

## Publier une fonctionnalité


Vous développez une fonctionnalité en collaboration?
Publiez une fonctionnalité sur le serveur distant pour qu'elle puisse être utilisée par d'autres utilisateurs.

 `$ git flow feature publish MYFEATURE`

![alt text](http://url/to/images/publish-feature.png)


## Récupérer une fonctionnalité publiée

Récupérer une fonctionnalité publiée par un autre utilisateur

`$ git flow feature pull origin MYFEATURE`

Vous pouvez suivre une fonctionnalité sur le serveur distant en utilisant

`git flow feature track MYFEATURE`

![alt text](http://url/to/images/pull-feature.png)

# Livraison/Release

Prépare la sortie d'une nouvelle version de production
Permet les corrections de bugs mineurs et la préparation des métadonnées de la release

## Commencer une livraison

Pour commencer une livraison, utilisez la commande git-flow release

Créer une branche de livraison basée sur la branche de développement.

 `$ git flow release start RELEASE [BASE]`
 
 ![alt text](http://url/to/images/start-release.png)

Vous pouvez si besoin ajouter le paramètre [BASE], correspondant au hash d'un commit à partir duquel commencera la livraison. 
Ce commit doit faire partie de la branche de développement.

Il est préférable de publier la branche de livraison après l'avoir créée pour permettre aux autres développeurs de commiter dessus. 
De la même manière que pour les fonctionnalités, utilisez cette commande:

 `$ git flow release publish RELEASE `

Vous pouvez suivre une livraison sur le serveur distant en utilisant

 `$ git flow release track RELEASE` 


# Terminer une livraison

Terminer une livraison est une des étapes majeures de cette méthode. Plusieurs actions sont réalisées :

- Fusionne la branche de livraison dans la branche 'master'
- Etiquette (tag) la livraison par son nom
- Fusionne la livraison dans la branche 'develop'
- Supprime la branche de livraison

 `$ git flow release finish RELEASE`
 
  ![alt text](http://url/to/images/finish-release.png)

N'oubliez pas de pousser vos étiquettes (tags) avec

 `$ git push --tags`


# Correctifs/Hotfixes

Les correctifs sont utiles quand il est nécessaire de corriger immédiatement l'état incorrect de la version en production
Ils peuvent se baser sur l'étiquette de la branche 'master' indiquant la version en production.

## Commencer un hotfix

Comme pour les autres commandes git-flow, un hotfix est commencé par

 `$ git flow hotfix start VERSION [BASE]`
 
 ![alt text](http://url/to/images/start-hotfix.png)

Ici, le paramètre VERSION indique le nom de la future release corrective. 
Vous pouvez si besoin spécifier le paramètre [BASE], correspondant au hash d'un commit ou au nom d'une branche à partir duquel s'appliquera le hotfix.

## Terminer un hotfix

En terminant un hotfix, il est fusionné dans les branches 'develop' et 'master'. 
De plus la fusion vers 'master' est etiquetée par la version du hotfix.

 `$ git flow hotfix finish VERSION`
 
 ![alt text](http://url/to/images/finish-hotfix.png)
 
 
# Commandes

![alt text](http://url/to/images/commandes.png)