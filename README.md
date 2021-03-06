# Dojo React - Product cart

Ce dojo est l'occasion parfaite de pratiquer l'affichage de listes, la gestion du state, des formulaires et des évènements !

Pour commencer, clonez ce dépot et placez-vous à l'interieur du dossier coresspondant.

## Lancer l'application

```sh
$ npm install && npm start
```

## Instructions

Le but général est de créer une petite application React permettant de gérer un panier de produits.

![Screenshot de l'application finale](https://i.imgur.com/TRUaDKk.png)

Jettez un oeil à `App.css` afin d'utiliser **uniquement** les classes existantes pour styliser l'application *a minima*. 

Conseil : *Comme d'habitude*, gardez bien votre console ouverte pendant le développement, pour ne pas laisser passer de warning ou d'erreur quelconque :)

### Etape 1 : Afficher les produits dans un tableau

Dans `App.js` vous avez quelques exemples de produits dans la constante `initialProductList`.

Il faut afficher ces 3 produits dans un tableau qui possèdera les colonnes  : 
- 'Produit' (`name`)
- 'Prix unitaire' (`price`)
- 'Quantité' (`quantity`)
- 'Prix total' (`price * quantity`)

### Etape 2 : Afficher le total de la commande

En dessous du tableau, affichez le montant total du panier, qui se calcule en faisant la somme des prix totaux (prix * quantité) des items du panier.

### Etape 3 : Permettre de changer la quantité d'un produit dans la liste 

Dans le tableau, la colonne 'Quantité' ne devrait contenir que des `<input>` (pensez au bon type d'input, avec des contraintes cohérentes comme on parle d'une quantité) : 
- Ces inputs doivent êtres **controllés par React**. 
- Les données des produits devront être gérées dans le `state`.
- Le prix total de l'item ainsi que le montant total de la commande devraient se mettre à jour automatiquement à l'édition d'une quantité pour un item de la commande.

### Etape 4 (BONUS) : Suppression d'un produit de la liste

Dès que l'on rentre une quantité de 0, une pop-up `window.confirm` apparait pour demander à l'utilisateur "Etes-vous sûr de bien vouloir retirer ce produit de la liste ?" : 
- S'il confirme, on le fait (sans blague !).
- Sinon sa saisie de quantité (0) est annulée (rien ne se passe, la quantité n'est pas mise à jour).

### Etape 5 (BIG BONUS) : Ajout d'un produit dans la liste

Creez un formulaire pour ajouter un produit : 
- Ce dernier contiendra deux champs : 'Nom' et 'Prix', ainsi qu'un bouton 'Ajouter'.
- Dès que l'on souhaite ajouter un produit, il faut s'assurer que le nom est bien présent et que la quantité a une valeur cohérente  (pensez aux contraintes d'input HTML5 !).
- Par défaut un nouveau produit dans la liste aura une quantité de 1.
- Un nouveau produit devra posséder un identifiant (`id`) généré aléatoirement au moment de la création.

