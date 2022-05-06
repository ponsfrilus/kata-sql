# Kata SQL

Ceci est un exercice permettant de pratiquer des requêtes SQL sur des
tables pré-définies.

> **À propos**
>
> ⓘ Ceci est la donnée d'un [kata], un _exercice de programmation_ qui se
> déroule généralement dans le cadre d'un [coding dojo]. Il est proposé aux
> membres du dojo de l'[EPFL] et fait partie d'une collection de différents
> katas identifiés par le tag [epfl-dojo-kata] sur GitHub. Vous êtes
> cordialement invité à essayer de le réaliser dans le langage de programmation
> de votre choix. Pour cela, un bon point de départ pour cela est de [forker] ce
> repository. Le «[stargazer]» en lui ajoutant une **☆** nous fait également
> très plaisir. Finalement, n'hésitez pas à l'améliorer en faisant des
> [pull requests]. Bonne lecture !

[kata]: https://fr.wikipedia.org/wiki/Coding_dojo#Kata
[coding dojo]: https://fr.wikipedia.org/wiki/Coding_dojo
[EPFL]: https://www,epfl.ch
[epfl-dojo-kata]: https://github.com/topics/epfl-dojo-kata
[forker]: https://docs.github.com/en/get-started/quickstart/fork-a-repo#forking-a-repository
[stargazer]: https://docs.github.com/en/get-started/exploring-projects-on-github/saving-repositories-with-stars
[pull requests]: https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request#creating-the-pull-request


## Concept

Vous êtes responsable de la communication de la discothèque "HelloDojo" qui
ouvrira prochainement ses portes. Vous avez récupéré des listes de personnes au
format SQL et dans le but d'exercer vos talents de marketing, vous avez besoin
d'en extraire des informations pertinentes.

Afin que d'autres personnes puissent faire de même, __vous devez consigner les
étapes pour reproduire votre travail le fichier [HowTo.md](HowTo.md)__. Dans un
monde idéal, vous avez __cloné le dépôt__ et ainsi vous pourrez également voir
les démarches effectuées par vos collègues et en profiter !

Si vous êtes arrivé au bout de l'exercice, vous pouvez derechef vous ajouter au
fichier [Jelaifait.md](Ivemadeit.md) dans une pull request. 

La documentation officielle de MySQL se trouve
[ici](https://dev.mysql.com/doc/refman/8.0/en/) et la page de
[StackOverflow](https://stackoverflow.com/tags/mysql/info) peut également
sérvir.


# Étapes

## Mise en place

Tout d'abord, vous devez vous débrouiller pour __importer les données__ dans un
système de gestion de base de données (SGBD) tel que MySQL. Toutes les options
vous sont ouvertes. Vous fournissez une explication sur ce choix dans le fichier
[HowTo.md](HowTo.md), et vous créez également un [schema.jpg](schema.png) 
permettant de visualiser les différentes tables de la base de donnée.


## Informations à récolter

### Générales
1. Pour commencer, vous désirez connaître le nombre de personnes que vous avez
   dans votre base de données (`people`).
   [ⓘ](https://dev.mysql.com/doc/refman/8.0/en/select.html "SELECT")
1. Comment trouver l'email de la personne dont le nom de famille est "Warren" ?
   [ⓘ](https://dev.mysql.com/doc/refman/8.0/en/select.html "WHERE")
1. Comment trier les résultats par ordre alphabétique croissant sur le nom de
   famille ?
   [ⓘ](https://dev.mysql.com/doc/refman/8.0/en/select.html "ORDER BY")
1. Il y a-t-il un moyen de limiter le nombre de résultat, par exemple en
   affichant uniquement les 5 premiers, toujours triés par nom de famille ?
   [ⓘ](https://dev.mysql.com/doc/refman/8.0/en/select.html "LIMIT")
1. Comment trouver les personnes qui ont un prénom ou un nom qui contient
   `ojo` ?
   [ⓘ](https://dev.mysql.com/doc/refman/8.0/en/string-comparison-functions.html#operator_like "LIKE")
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
1. Il y a-t-il des doublons dans la table people ?
   [ⓘ](https://dev.mysql.com/doc/refman/8.0/en/select.html "DISTINCT")

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
1. Afin de partager les informations présentes dans cette vue, vous l'exporter
   au format CSV afin que vos collègues puissent la visualiser dans un tableur.

### Finances
1. En vue de l'ouverture, le directeur a déjà acheté des caisses enregistreuses.
   Vous savez également que des bons et les cartes de membres pourront-être
   achetés sur le site Internet. Modifiez la base de donnée existante en
   ajoutant une table `expenses` qui permettra d'ajouter les dépenses de chaque
   membres.
1. Modifier la vue `HelloDojo` pour ajouter le total des dépenses par membre.
