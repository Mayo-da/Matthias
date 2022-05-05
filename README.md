# Matthias

Ennoncé
Nous allons dynamiser le template blog de bootstrap:
https://getbootstrap.com/docs/5.1/examples/blog/
 Sammy Dieleman            EFP – 2021-2022          LPB – PHP_1_blog÷
 
1. Préparation
1. Se rendre sur https://getbootstrap.com/docs/5.1/examples/ et télécharger l'archive contenant tous les exemples.
2. Charger le blog dans votre navigateur
3. Supprimer les exemples inutiles, ne garder que le blog (lisez le code source
pour savoir ce que vous pouvez supprimer)
4. Changer le titre du blog (Large) à votre guise
5. Se connecter à GitHub et créer un repository LPB-Blog, avec un fichier readme.md
6. Lancer GitHub Desktop et copier l'énnoncé de l'exercice dans le fichier readme.md
7. Ouvrir le dossier de travail dans VS Code
8. Copier le blog dans ce répertoire
9. Commit avec le message "Template de base du blog"
10. Push
Sammy Dieleman            EFP – 2021-2022          LPB – PHP_1_blog


2. Création des pages
1. Pour chaque item du menu (World, U.S., Technology, Design, Culture, Business, Politics, Opinion, Science, Health, Style, Travel), créer une page qui ne contiendra que les 2 derniers articles (Another blog post & New Feature)
Commit avec le message "Création des pages individuelles"
2. Changer le titre de chaque article en World 1 & World 2 pour la page World, U.S. 1 & U.S. 2, pour la page U.S. etc..
Commit avec le message "Modification des titres de page"
3. Changer les deux cartes (en dessous du cadre noir) pour que leur catégorie (de base World et Design) reflète la page courante (donc uniquement World, U.S. etc..)
Commit avec le message "Changement des cartes"
Vous avez maintenant 13 pages HTML, une page d'accueil et 12 pages de catégorie.
Vous avez, bien entendu, fait attention à la cohérence dans votre convention de nommage des 12 fichiers
Le nom de fichier page U.S. ne doit pas contenir les points de l'acronyme.
Quand tout est cohérent et correspond à l'énnoncé, réaliser un dernier commit avec le
message "Fin de la création des pages individuelles" et un push final.
Retourner sur le site GitHub, dans votre repository et contempler le travail effectué
Sammy Dieleman            EFP – 2021-2022          LPB – PHP_1_blog


3. Création du menu
Ces pages statiques doivent maintenant devenir un sites statique: il faut les lier grâce au menu.
1. Créer les liens nécessaires dans le menu des 13 pages et tester votre site. 2. Commit avec un message concis et claire et push


4. DRY
Si vous changez le nom de votre site, ou une catégorie dans le menu, vous devez changer 13 pages, sans faute.
Ce travail est fastidieux et sujet aux erreurs.
Nous allons utiliser PHP et les requêtes HTTP pour nous simplifier la tâche.
Pour cela nous allons découper la page en partiel:
1. Déterminer les parties du site qui sont communes
2. Créer les fichiers HTML correspondant à ces parties (nommage !)
3. COPIER le code HTML de chaque partie dans son fichier
4. Commit & Push (attention au message, clair et concis)
Pourquoi copier ? Le site local doit rester fonctionnel à tout moment, on ne sacrifie pas le travail effectué
Sammy Dieleman            EFP – 2021-2022          LPB – PHP_1_blog

 
5. HTTP GET & PHP $_GET
Dans votre répertoire de travail courrant:
1. Créer un fichier test_get.php
2. Ecrire un boilerplate HTML
3. Ecrire le code suivant dans le <body> <pre>
     <?php
        var_dump($_GET);
?> </pre>
4. Charger, via le serveur, la page dans votre navigateur et concatener dans l'URL 1. ?text=hello
2. &categorie=world
3. &key=value
Pour chaque étape, constater la modification du contenu de la super global $_GET
Sammy Dieleman            EFP – 2021-2022          LPB – PHP_1_blog

6. PHP include & require
Dans votre répertoire de travail courant:
1. Créer un fichier test_partiels.php (sans boilerplate)
2. Y inclure les partiels créés au point 4 grâce à l'expression PHP include
include 'nomdufichier.html';
https://www.php.net/manual/en/function.include.php
3. Test, commit, push
4. Utiliser require au lieu de include https://www.php.net/manual/en/function.require.php
5. Test, commit, push
  Sammy Dieleman            EFP – 2021-2022          LPB – PHP_1_blog

7. Tire ton plan
Vous avez maintenant toutes les clés en main pour automatiser votre blog. Vos connaissances sont encore partielles et fraîches mais suffisantes,
1. déterminer un moyen de combiner $_GET & include pour charger dynamiquement le contenu principal de chaque page
2. adapter le partiel contenant le menu pour qu'il utilise le format d'adresse mis au point
3. Test, commit, push
4. Que se passe-t-il lorsque :
1. Il n'y a pas de paramètres GET et donc $_GET est vide ?
2. Les paramètres GET sont invalides (en suivant le format d'URL, demander à votre site la catégorie (inexistante) "Training"
5. Test, commit, push
