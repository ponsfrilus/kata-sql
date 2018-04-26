# EPFL Dojo - Requêtes SQL
Le but est d'avoir un exercice permettant de pratiquer des requêtes SQL sur des
tables pré-définies.

## Concept
Vous êtes responsable de la communication de la discothèque "HelloDojo" qui
ouvrira prochainement ses portes. Vous avez récupéré des listes de personnes au
format SQL et dans le but d'exercer vos talents de marketing, vous avez besoin
d'en extraire des informations pertinantes.

Afin que d'autres personnes puissent faire de même, vous devez noter toutes les
étapes dans le fichier [HowTo.md](HowTo.md). Dans un monde idéal, vous avez
cloné le dépôt et ainsi vous pourrez également voir les démarches effectuées par
vos collègues et en profiter !

# Etapes

## Mise en place
Tout d'abord, vous devez vous débrouiller pour importer les données dans un
système de gestion de base de données (SGBD) tel que mysql.

## Informations à récolter

### Générales
1. Pour commencer, vous désirez connaître le nombre de personnes que vous avez
   dans votre base de données (`dojo-people`).
1. Il y a-t-il des doublons ?
1. Comment les trier par ordre alphabétique croissant sur le nom de famille ?
1. Il y a-t-il un moyen de limiter le nombre de résultat, par exemple en
   affichant uniquement les 10 premiers ?
1. Comment trouver les personnes qui ont un prénom ou un nom qui contient `ojo` ?

### Invitations
1. Pour l'ouverture, vous désirez lister tous le membres de plus de 18 ans
  a. et de moins de 60 ans
  a. qui ont une addresse email valide
1. Avec ces membres, vous désirez faire une liste sous le format suivant
   `Prénom Nom <email@provider.com>;` afin de pouvoir la copier/coller dans
   votre client email.
1. Avec les informations contenues dans la table `dojo-people`, pourrait-on
   approximer le nombre de personnes habitant en Suisse ?

### Countries
1. Pour un futur formulaire d'inscription sur un site Internet, vous voulez
   pré-macher votre travail en préparant les données des pays pour les options
   d'un `<select>`. Préparer la requête qui permet d'obtenir la liste d'options
   sous la forme: `<option value="XXX">XXX</option>`.
1. Quelle serait une solution pour avoir cette liste disponible en français et
   en anglais lorsque le site sera traduit ?

### Jointure
1. Vous avez remarqué que la table `countries.sql` contient une colonne `tld`.
   Trouvez un moyen d'afficher le nom du pays en anglais en fonction du `tld` de
   l'adresse email de la personne.
1. Pourrait-on afficher "Country unkown" si l'email est vide ou que le `tld` ne
   match aucun pays ?

### Vue
1. Pour faciliter vos futurs requêtes, vous créer une vue qui contient les
   colonnes suivantes:
    ...
