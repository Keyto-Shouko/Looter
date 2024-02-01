# Looter Questions

# App-Basic

## 🔧 Exercice 1

1) Essayez de lancer l’application (ou de la visualiser dans la preview), XCode devrait vous afficher une erreur. Que manque-t-il ? Et pourquoi ?
Il manque un ID pour avoir la List, solution : List(loot, id: \.self)

## 🔧 Exercice 2
1) Expliquez le changement que j’ai effectué par rapport à l’exemple précédent.
Création d'un bouton "Ajouter", ajout d'un ForEach pour faire la liste

2) Pourquoi utiliser un ForEach ? Quel est son rôle ? Et pourquoi séparer le bouton du ForEach ?
Le ForEach permet plus de contrôle sur la liste et afficher d'autres éléments en plus de la liste (un boutton par exemple) dans le composant List.

## 🔧 Exercice 3
1) Testez ce code, fonctionne-t-il ? Pourquoi ?
Non, il faut le wrapper @State.

2) Expliquez pourquoi maintenant cela fonctionne ?
Le wrapper @State rend la variable "loot" modifiable.

# Ajout-item
## 🔧 Exercice 1
1) Cliquez sur le bouton “Ajouter”, que se passe-t-il ? Pourquoi cela ne marche pas ?
On ne peut pas modifier inventory, il faut ajouter @StateObject.

2) Si vous ajoutez plusieurs items, que se passe-t-il dans la console XCode, vous devriez avoir un message d’erreur, expliquez pourquoi ?

## Exercice 2

1) Pourquoi cela fonctionne de nouveau ?

2) Pourquoi utiliser @StateObject plutôt que @ObservedObject ou @State ?
StateObject n'écrase pas le tableau alors que @State ne compare que les types basiques.