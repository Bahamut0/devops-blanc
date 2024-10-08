# crucihelp

 **Fonctionnement général:**
 
 1. **Chargement du dictionnaire:** Le module charge un dictionnaire de mots depuis un fichier texte.
 2. **Recherche de mots:** L'utilisateur saisit un mot à rechercher, qui peut contenir des caractères génériques (représentés par le caractère '?'). 
 3. **Affichage des résultats:** Le module affiche tous les mots du dictionnaire qui correspondent au motif de recherche.
 
 **Exemple d'utilisation:**
 
## Pour rechercher tous les mots de 4 lettres commençant par 'C' et se terminant par 'T', vous pouvez saisir le motif "C??T".
 
 **Note:** Les mots du dictionnaire sont automatiquement convertis en majuscules pour les recherches.
 
 **Modules utilisés:**
 
 * `re`: Module pour l'utilisation d'expressions régulières, permettant la recherche de motifs avec des caractères génériques.
 
 **Limitations:**
 
 * Les caractères génériques ne peuvent représenter qu'une seule lettre.
 * Le dictionnaire est chargé en mémoire, ce qui peut limiter la taille des dictionnaires utilisables.


## Partie CICD :

**Branches:**

* `main` : branche de production

* `stage` : branche de test

* `features` : branche de développement

* `feature-XXX` : branche personnelle provisoire à merger dans features

**Workflow:**

* En cas de push d'une branche `feature-XXX`, une pull request est créée avant merge vers la branche features

* En cas de validation de la pull request la branche est mergée dans la branche `stage`

* En cas de merge vers la branche stage, les tests sont effectués

* En cas de tests réussis, une merge est effectuée sur la branche `main`

* En cas de merge sur la branche main, un tag et une release sont créés


