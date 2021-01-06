# EPFL Dojo - Requêtes SQL
Le but est d'avoir un exercice permettant de pratiquer des requêtes SQL sur des
tables pré-définies.

## Concept
Vous êtes responsable de la communication de la discothèque "HelloDojo" qui
ouvrira prochainement ses portes. Vous avez récupéré des listes de personnes au
format SQL et dans le but d'exercer vos talents de marketing, vous avez besoin
d'en extraire des informations pertinantes.

Afin que d'autres personnes puissent faire de même, __vous devez noter toutes
les étapes dans le fichier [HowTo.md](HowTo.md)__. Dans un monde idéal, vous
avez __cloné le dépôt__ et ainsi vous pourrez également voir les démarches
effectuées par vos collègues et en profiter !

La documentation officielle de MySQL se trouve
[ici](https://dev.mysql.com/doc/refman/8.0/en/) et la page de
[StackOverflow](https://stackoverflow.com/tags/mysql/info) peut également sérvir.

# Étapes

## Mise en place
Tout d'abord, vous devez vous débrouiller pour __importer les données__ dans un
système de gestion de base de données (SGBD) tel que mysql. Toutes les options
vous sont ouvertes. Vous créez également un [schema.jpg](schema.png) de votre
base de donnée.

## Informations à récolter

### Générales
1. Pour commencer, vous désirez connaître le nombre de personnes que vous avez
   dans votre base de données (`people`).
1. Il y a-t-il des doublons ?
1. Comment trouver l'email de la personne dont le nom de famille est "Warren" ?
1. Comment trier les résultats par ordre alphabétique croissant sur le nom de
   famille ?
1. Il y a-t-il un moyen de limiter le nombre de résultat, par exemple en
   affichant uniquement les 5 premiers, toujours triés par nom de famille ?
1. Comment trouver les personnes qui ont un prénom ou un nom qui contient
   `ojo` ?
1. Quelles sont les 5 personnes les plus jeunes ? Et les plus agées ?
   Attention aux personnes qui ne sont pas encore nées...
1. Comment trouver l'age, en année, des personnes ?
1. Comment peut-on trouver la moyenne d'age des personnes présentes dans la
   table ?
1. Votre designer travail sur les cartes de membre et il a besoin de savoir
   quelle est la personne avec le plus long prénom et le plus long nom.
1. Ne sachant encore pas exactement la manière dont le layout des cartes de
   membres sera organisé, il aimerait également savoir qui sont les 3 personnes
   qui ont, mis ensemble, la pair nom + prénom la plus longue.

### Invitations
1. Pour l'ouverture, vous désirez lister tous les membres de plus de 18 ans,
    * et de moins de 60 ans,
    * qui ont une addresse email valide.
1. Pour faciliter la lecture vous ajoutez une colonne `age` dans le résultat
   de votre requête.
1. Avec ces membres, vous désirez faire une liste sous le format suivant
   `Prénom Nom <email@provider.com>;` afin de pouvoir la copier/coller dans
   votre client email.
1. Avec les informations contenues dans la table `people` (sans jointures),
   pourrait-on approximer le nombre de personnes habitant en Suisse ?

### Countries
1. Pour un futur formulaire d'inscription sur un site Internet, vous voulez
   pré-macher votre travail en préparant les données des pays pour les options
   d'un `<select>`. Préparer la requête qui permet d'obtenir la liste d'options
   sous la forme : `<option value="XXX">XXX</option>`.
1. Quelle serait une solution pour avoir cette liste disponible en français et
   en anglais lorsque le site sera traduit ?

### Jointure
1. En utilisant la table de jointure `countries_people.sql`, lister les
   personnes habitant en Suisse.
1. De la même manière, lister les personnes qui n'habitent pas en Suisse.
1. Comment lister les personnes (nom et prénom) qui habitent dans les pays
   limitrophe de la Suisse ? (i.e France, Allemagne, Italie, Autriche, Lischenchtein)
1. Vous souhaitez savoir combien il y a de personnes par pays, afin de savoir si
   votre table people a suffisament de personnes en suisse et combien de
   personnes sont étrangères.
1. Quels sont les pays qui ne possèdent pas de personnes ?
1. Il y a-t-il des personnes qui sont liées à plusieurs pays ?
1. Il y a-t-il des personnes liées à aucun pays ?
1. Comment pourrait-on afficher le pourcentages de personnes par pays ?

### Procédures
1. Vous avez remarqué que la table `countries.sql` contient une colonne `tld`.
   Trouvez un moyen d'afficher le nom du pays en anglais en fonction du `tld` de
   l'adresse email de la personne.
1. Pourrait-on afficher "Country Unkown" si l'email est vide ou que le `tld` ne
   match aucun pays ?
1. Comment pourrait-on avoir accès à un méchanisme qui trouve automatiquement le
   `tld` des addresses emails ?

### Vue
1. Pour faciliter vos futurs requêtes, vous créer une vue `HelloDojo` qui
   contient les colonnes suivantes :
    * Toutes les informations de la table `people` ;
    * Une colonne `age` ;
    * Une colonne formatée avec `Prénom Nom` (i.c. majuscules) ;
    * Une colonne avec le nom du pays en Français.

### Finances
1. En vue de l'ouverture, le directeur a déjà acheté des caisses enregistreuses.
   Vous savez également que des bons et les cartes de membres pourront-être
   achetés sur le site Internet. Modifiez la base de donnée existante en
   ajoutant une table `expenses` qui permettra d'ajouter les dépenses de chaque
   membres.
1. Modifier la vue `HelloDojo` pour ajouter le total des dépenses par membre.
