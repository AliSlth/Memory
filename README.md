# Projet Memory

Petit jeu de memory où les joueurs peuvent saisir leurs noms et choisir un niveau de difficulté avant de commencer à jouer.
Technologies utilisées: HTML, CSS, JavaScript, jQuery
Les images sont libres de droit, obtenues sur le site https://pixabay.com/fr/

## Structure de la page

### Zone de formulaire
- Visible au départ puis cachée après validation du formulaire
- Permet aux joueurs de saisir leurs noms et de choisir la difficulté du jeu

### Zone de jeu
- Comprend la table de Memory avec des cartes face verso

## Fonctions clés

- **start()** : 
  - Initialise le jeu en récupérant les noms des joueurs et la difficulté choisie
  - Affiche les noms des joueurs et la table de jeu correspondante

- **turn(card)** : 
  - Retourne une carte face recto.

- **flip()** : 
  - Retourne les cartes face verso si elles ne correspondent pas

- **score()** : 
  - Calcule et met à jour les scores des joueurs en fonction du tour

- **highlight()** : 
  - Met en évidence le nom du joueur actif

- **end()** : 
  - Indique le gagnant ou l'égalité lorsque toutes les paires sont trouvées

## Évènements

- Lors d’un clic sur une image (le script vérifie si la carte est bien face verso), elle est retournée
- Le script vérifie ensuite si une ou deux cartes ont été retournées
  - En cas de deux cartes retournées, il vérifie si elles correspondent en comparant la source d’image
    - Si oui, il augmente le compteur de paires et met à jour les scores
    - Si elles ne correspondent pas, les cartes sont retournées face verso et le tour des joueurs est échangé

## Variables

- **player1** et **player2** : Stockent les noms des joueurs
- **level** : Contient le niveau de difficulté choisi pour le jeu
- **pairCount** : Compte le nombre de paires correctement identifiées
- **card1** et **card2** : Représentent les cartes retournées pour comparaison
- **score1** et **score2** : Gardent en mémoire les scores des joueurs
- **currentPlayerTurn** : Indique le numéro du joueur actuel (1 ou 2)

## Optimisations

Quelques bugs ont été remarqués, notamment lors de clics trop rapides. On pourrait apporter d'autres améliorations au niveau des fonctionnalités, par exemple :

- D’autres niveaux de difficulté ou bien un choix de thème
- Une fonction permettant de mélanger les cartes à chaque début de jeu
- Une fonction permettant de directement accéder au menu de sélection
- Bouton permettant de recommencer la partie directement
