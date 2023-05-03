Bonjour,

Je remarque un effort pour tenter de réaliser la totalité du projet. Malheureusement, ce dernier ne fonctionne pas et il est très difficile de l'utiliser dans l'état. Je vais donc te faire un retour sur le code du projet.

## ROUTES ##
- Route de démarrage non-fonctionnelle. J'ai été obligé d'aller la chercher dans le code.
- Routes finalement toutes non-fonctionnelles. 😅
- Manque d'explication pour comprendre le projet ou projet non-fonctionnel. 

## OUBLI ## 
- Restant du projet HTML dans docs. La consigne indique bien qu'il est nécessaire de supprimer les traces de ce dernier. 

## REMARQUES MODEL ##
- Il est plus simple d'utiliser self::class au lieu de spécifier le nom du model utilisé. Cela pourrait éviter des erreurs  😅
- Les requêtes SQL ne sont pas sécurisées ; utilisation du prepare et bindValue https://www.php.net/manual/fr/pdo.prepare.php 
- Les requêtes ne sont pas correctes ; tu ajoutes des "{" et des "}". Si le prénom est "Henry", ça donne donc : " firstname='{henry}' "
- Je ne peux que te conseiller de stocker tes requêtes dans une variable avant d'utiliser la fonction "preparer", c'est bien plus lisible et tu pourras faire tes requêtes sur plusieurs lignes : Gain de lisibilité (ligne 80 du Model Teacher) 😉
- "$pdo->exec" ne va pas te renvoyer le nb d'éléments. Tu dois utiliser la fonction "->rowCount()" sur ton PDO statement pour ça.

## CONTROLLER ##
- Tu dois faire attention à tes commentaires. Du vieux code commenté qui prend 5s à reproduire, c'est des octets en plus ; // var_dump($_POST);die; (l. 39 Teacher Controller)  😁
- Quand tu veux décrire une fonction, sa description doit avoir un intérêt. Ecrire "edit un teacher" revient à juste écrire le nom de ta fonction une seconde fois... La description doit avoir un intérêt et doit permettre de comprendre rapidement la fonction ; Les données envoyées proviennent de POST / GET ? D'où ça vient ? D'un formulaire ? 
- La nomination laisse à désirer. Appeler ta fonction "AddTeacher" n'est pas intéressant. Nous sommes dans le controller "Teacher", inutile de le préciser de nouveau. Inutile de préciser dans le nom du fonction si celle-ci utiliser des données en POST ou GET, cette information pourrait bien changer à l'avenir. Or, si ceci change, tu devrais modifier le nom de ta fonction à chaque endroit où tu utilises cette dernière ! 
- Manque de précision sur les libellés des erreurs ; dans le cas actuel, le prénom est juste vide si erreur il y a à ce sujet. Le statut ne peut pas être à empty (sans modification du html). Tu devrais plutôt utiliser les chiffres dans le select pour éviter une erreur 
- Evites d'utiliser "dump", ce n'est pas très esthétique et c'est dommage de ne pas utiliser ton tableau des erreurs débuté juste au-dessus. 
- Dans "teacherUpdatePost", tu fais une erreur très gênante ; Une erreur très importante pourrait te causer des torts ; tu modifies ton élément courant sans vérifier les potentielles erreurs au préalable. 😉

## VIEWS ## 
- Généralement, tes vues UPDATE / ADD sont identiques. Tu devrais essayer d'utiliser la même vue, ça te permettra d'éviter de la maintenance fastidieuse par la suite. 
- Tes vues partagent "<div class="container my-4">" en début de vue, ne penses-tu pas qu'il aurait été avantageux de placer cette div dans un fichier parent ? Le jout où tu veux passer en my-5, tu gagneras beaucoup de temps. 😉


Un peu d'effort, tu es sur la bonne voie, mais tu dois renforcer tes connaissances.
