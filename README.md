# Exercice d'accessibilité des contenus

## Équipe
- Léa Marois
- Prénom nom

## Objectifs
- Expérimenter le versionnage de fichiers avec GIT
- Acquérire des compétences en accessibilité des contenus

## Prérequis
- Avoir lu et pris connaissance des notes du cours 10
- Avoir un compte GitHub
- Avoir installé et configurer GIT sur votre ordinateur
- Avoir installé l'outil CCA (colour-contrast-analyzer)

## Instructions

### 0. 
- Initialiser un dépôt GIT dans le dossier du projet
- Créer un fichier `index.html` et un fichier `style.css`

### 1.	Donner une alternative textuelle aux images

#### 1.1 Baliser dans le fichier `index.html` les images du dossier `1-textes-alternatifs` 

Pour vous guider dans le choix des balises, des attributs et des valeurs d'attributs, utiliser l'arbre de décision et référez-vous aux notes de cours.

#### 1.2 Évaluer la pertinence des contenus textuels alternatifs

Pour chacune des pages ci-dessous, les textes alternatifs sont-ils adéquats ?Commenter votre observation. Pourrait-on faire mieux ? Donnez un exemple de ce que vous proposeriez.

- https://www.sail.ca/fr/chaussures/junior/multi-sport-et-plein-air 
Les textes alternatifs sont adéquat pour les photos et le logo mais nulpart d'écritons les couleurs
[capture-écran](images/1-textes-alternatifs/1-2/sail_plein_air.png)
-----


- https://amzn.to/2NnbKPN 
Les textes alternatif décrit la même choses de se qui est écrit en dessous de l'images et on même des ... lorsque le texte est trop long. j'aurais peut-être essayer de mettre un description des images.
[capture-écran](images/1-textes-alternatifs/1-2/amazon.png)
-----


- https://www.lesoleil.com/  
Ils ont tous le nom de l'article en temp que texte alternatif mais il n'a pas de texte alternatif pour le bouton recherche.
[capture-écran](images/1-textes-alternatifs/1-2/leSoleil.png)
-----


- https://www.rad.ca/  
Aucun texte alternatif au moins certain article on voit le titre mais même sur celle qui est seulement une images il n'a pas de texte alternatif.
[capture-écran](images/1-textes-alternatifs/1-2/RadioCanada.png)
-----


Astuce  
Parfois, l’affichage des alt ne donnent pas un résultat facile à lire… lorsque cela se produit, faites un clic droit de la souris et choisir inspecter pour positionner l’inspecteur de DOM sur le HTML de l’image.
Essayer d’identifier l’emplacement du alt et puis regarder s’il y a une description tout de suite après.

### 2.Vérifier les contrastes de couleurs

#### 2.1	Utiliser l’outil d’analyse de contraste des couleurs (CCA) pour identifier les problèmes de contrastes sur cette page : http://2016.webaquebec.org/

Pour chaque problème de contraste identifié,
documenter le problème par une capture-écran incluant dans son cadre, la zone fautive à gauche et à droite, les résultats détaillés de l’outil, tel que démontré dans l’exemple ci-dessous.

Sauvegarder les captures dans le dossier images. Compléter les liens ci-dessous:
- [Contraste insuffisant 1](images/2-contrastes-couleurs/constraste1.png)
- [Contraste insuffisant 2](images/2-contrastes-couleurs/constraste2.png)
- [Contraste insuffisant 3](images/2-contrastes-couleurs/constraste3.png)

### 3. Structurer avec les h1-h6 une table des matières

#### 3.1 Vérifier la structure

D’après les captures-écrans que vous trouverez dans le dossier [images/3-table-des-matieres_h1-h6/3-1/](images/3-table-des-matieres_h1-h6/3-1) , est-ce que la table des matières du document est correcte?  

Sinon, expliquez le problème en vous basant sur les règles de base énoncées dans les notes de cours. 

__Tutoriel sur les formulaires du w3c__  
[Article](images/3-table-des-matieres_h1-h6/3-1/tuto-form-w3c.pdf)  

[Table des matières (outline)](images/3-table-des-matieres_h1-h6/3-1/tuto-form-w3c-outline.png) 

Réponse : 
----
Le h1 est le titre de l'article et les h2 sont les sous-titre de cette article. Parfait.

----
----

__L’affaire Savtchenko__ 
[Article](images/3-table-des-matieres_h1-h6/3-1/article-savtchenko.pdf)  
[Table des matières (outline)](images/3-table-des-matieres_h1-h6/3-1/article-savtchenko-outline.png) 
  
Réponse : 
----
Les 4 premiers h2 de la page ne devrais pas être des h2 sois des forms des bouton mais pas des h2. Et tout les autres h2 de la page ne devrais pas être la non plus, il ne sont pas des sous-titre du h1 il sont des choses dans la page aucune relation avec le contenus du h1. Le premier h2 est avec le h1 mais c'est le texte intro de l'article et pas un sous-titre.

----
----


#### 3.2 S'exercer à bien structurer

- Ouvrir la capture-écran [concevoir-un-design-sans-la-couleur](images/3-table-des-matieres_h1-h6/3-2/concevoir-un-design-sans-la-couleur.pdf) que vous trouverez dans le dossier `sources > h1h6-partie-2` dans le logiciel PhotoShop.  
- Ajouter un calque de blanc à 50% de transparence
- Dans un 3e calque, par-dessus, identifiez les titres et leurs niveaux (h1-h6) de manière voyante (couleur rouge et font-size suffisant)
- Sauvegarder au format .psd ou .png dans le même dossier.
- [Relier ce fichier-réponse ici](images/3-table-des-matieres_h1-h6/3-2/concevoir-un-design-sans-la-couleur.png)

### 4. Baliser un tableau de données pour qu’il soit accessible

D’après la capture-écran et le texte fourni dans le dossier [4-tableau-de-donnees](images/4-tableau-de-donnees), balisez de manière accessible ce tableau de données.  
  
Votre tableau de données doit comporter un titre (caption) : 

> "Recommandations de consommation de poissons selon l’âge, le sexe et la condition physique".  


Les __entêtes de rangées et de colonnes__ doivent être balisées comme des `<th>` plutôt que des `<td>` et puisque le tableau est *complexe*, vous devez utiliser des attributs `id` dans les `<th>`. 

Chaque cellule `<td>` du tableau doit avoir un attribut headers avec comme valeur(s), le ou les identifiants de ses entêtes de colonnes et de rangées.

Styler le tableau conformément au fichier [consommation-poissons.pdf](images/4-tableau-de-donnees/consommation-poissons.pdf).

#### Ressources
•	balisage accessible d’un tableau (voir les notes du cours 10)
•	balisage html : https://www.w3schools.com/TAGs/tag_table.asp
•	balisage css de tableau: https://www.w3schools.com/css/css_table.asp





