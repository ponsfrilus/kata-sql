# HelloDojo Marketing

Ce fichier permet de documenter (et logguer) les étapes que vous avez suivies pour réaliser les demandes du [README.md](README.md).

## Mise en place
Voici les étapes que j'ai suivies pour installer XXX et importer les tables.
e.g. `CREATE SCHEMA `kata-sql` DEFAULT CHARACTER SET utf8mb4 ;`
J'ai choisi d'utiliser XXX comme client de base de donnée.
J'ai généré le schéma avec XXX:

![Mon MLD](schema.png "Mon MLD généré avec XXX").


## Informations à récolter

### Générales
1. La table `people` contient XXX personnes, ma requête est:  
  `SELECT XXX FROM XXX`
1. La table `people` contient XXX doublons, ma requête est:  
  `SELECT XXX FROM XXX`
1. La table `people` est triée par nom de famille, ma requête est:  
  `SELECT XXX FROM XXX`
1. Je trouve les 5 premiers enregistrements de la table `people`, ma requête est:  
  `SELECT XXX FROM XXX`
1. Je trouve tous les enregistrements de la table `people` qui contiennent `ojo`, ma requête est:  
  `SELECT XXX FROM XXX`
1. Les 5 personnes plus agées sont `LIST`, ma requête est:  
  `SELECT XXX FROM XXX`
1. Les 5 personnes plus jeunes sont `LIST`, ma requête est:  
  `SELECT XXX FROM XXX`
1. La moyenne d'age est `NUMBER`, ma requête est:  
  `SELECT XXX FROM XXX`
1. Le plus long prénom est `TEXT`, ma requête est:  
  `SELECT XXX FROM XXX`
1. Le plus long prénom est `TEXT`, ma requête est:  
  `SELECT XXX FROM XXX`
1. La plus longue pair nom + prénom est `TEXT`, ma requête est:  
  `SELECT XXX FROM XXX`

### Invitations
1. Pour lister tous le membres de plus de 18 ans:  
  `SELECT XXX FROM XXX`
  a. et de moins de 60 ans:  
     `SELECT XXX FROM XXX`
  a. qui ont une addresse email valide:  
     `SELECT XXX FROM XXX`
1. Pour ajoutez une colonne `age`:  
   `SELECT XXX FROM XXX`
1. Pour générer une liste contenant `Prénom Nom <email@provider.com>;`:  
   `SELECT XXX FROM XXX`
1. Avec cette requête:  
     `SELECT XXX FROM XXX`  
   je peux estimer que `NUMBER` personnes habitent en Suisse.

### Countries
1. La requête qui permet d'obtenir la liste d'options
   sous la forme: `<option value="XXX">XXX</option>` est:  
   `SELECT XXX FROM XXX`
1. Pour avoir la liste d'options en plusieurs langues, je procède de la manière suivante:  
   `STRING`

### Jointure
1. Avec cette requête:  
     `SELECT XXX FROM XXX`  
   je sais que `XXX` habitant en Suisse.
1. Avec cette requête:  
     `SELECT XXX FROM XXX`  
   je sais que `XXX` n'habitant pas en Suisse.
1. Avec cette requête:  
     `SELECT XXX FROM XXX`  
   je liste les membres habitants en France, Allemagne, Italie, Autriche et Lischenchtein.
1. Cette requête:  
     `SELECT XXX FROM XXX`  
   permet de compter combien il y a de personnes par pays.
1. Cette requête:  
     `SELECT XXX FROM XXX`  
   liste les pays qui ne possèdent pas de personnes.
1. En exécutant cette requête:  
     `SELECT XXX FROM XXX`  
   je sais que `NAME`, `NAME` et `NAME` sont liés à plusieurs pays.
1. En exécutant cette requête:  
     `SELECT XXX FROM XXX`  
   je sais que `NAME` est lié à un pays qui n'existe pas dans la base.
1. De la manière suivante:  
     `SQL`  
   nous pouvons afficher le pourcentages de personnes par pays.


### Procédures

1. Cette requête permet d'extraire `tld` de l'adresse email et de le lier à la table `countries`:  
    `SELECT XXX FROM XXX`  
1. Pour ajouter une chaine si la jointure ne retourne rien, j'ai procédé de la manière suivante:  
     `STRING`
1. Avec `STRING`, nous pouvons partager le mécanisme qui extrait le `tld`.

### Vue
1. J'ai créé une vue bien pratique contenant toutes les infomrations utiles à un humain. Ma requête est:  
   `CREATE XXX`

### Finances
1. J'ai créé une table pour les finances. Ma requête est:  
   `CREATE XXX`
1. J'ai modifié la vue en y ajoutant les finances. Ma requête est:  
   `UPDATE XXX`
