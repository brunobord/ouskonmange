# Où va-t-on manger ?

Tout le monde se pose cette question, le midi, avec les collègues.
Si personne n'ose se décider, voilà un outil approprié.

Il faut aller sur :

    http://brunobord.github.io/ouskonmange/

et tu auras un tirage aléatoire parmi 3 valeurs. Bon... ça sera pas très
satisfaisant.


## Alors à toi de jouer.


Soit tu forkes le dépôt source sur Github et édites le fichier `data.json` et 
tu te débrouilles pour avoir une liste JSON d'items sous la forme :

    [
        {"name": "Pizza Gino"},
        {"name": "Au buffet de la gare"},
        {"name": "Chez Dédé"}
    ]

Auquel cas tu pourras aller sur:

    http://[monusername].github.io/ouskonmange/

Soit tu clones ce dépôt sur un serveur à part et tu accèdes à l'URL de la page
tout naturellement. Et tu as toujours à modifier les données JSON pour te donner
le choix.


Soit tu utilises l'URL de la Github Page comme ceci :

    http://brunobord.github.io/ouskonmange/?data=premier+choix,deuxième+choix,troisième+choix

Tu peux même essayer de conserver cette URL dans tes signets, ça fonctionnera
toujours.

Soit... tu as accès à un serveur web sur lequel tu peux disposer d'une URL qui
renvoie la liste des restaurants au format JSONP, sous la forme suivante :

    ouskonmange(
        [{name: "toto"},
        {name: "meuh"}]
    )

**Note importante :** il est capital de conserver le nom ``ouskonmange`` comme
callback. Sinon, ça plante.

Disons que cette réponse est appelable à l'adresse http://example.com/restaurants.jsonp

Tu peux alors utiliser l'URL suivante :

    http://brunobord.github.io/ouskonmange/?source=http://example.com/restaurants.jsonp




## Licence et autres billevesées

Ce projet est sous licence WTFPL.

J'utilise:

* [Kube](http://imperavi.com/kube/)
* La police de caractère [PT Sans](http://www.google.com/fonts/specimen/PT+Sans)
