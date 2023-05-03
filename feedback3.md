Bonjour,

Malheureusement, le projet n'est pas assez avancé et les connaissances ne sont pas démontrées. Pour autant, je remarque que le listing aurait pu fonctionner, mais il aurait été nécessaire d'y consacrer un peu plus de temps.

## ROUTES ##
- Aucune redirection en arrivant sur le site, il est donc difficile de le tester. 
- Les routes ne sont pas présentes dans tes fichiers. Un fichier adéquat t'aiderait à les configurer.

## REMARQUES MODEL ##
- Il est plus simple d'utiliser self::class au lieu de spécifier le nom du model utilisé. Cela pourrait éviter des erreurs  😅
- De nombreux manquements ; add, update, ... Les models sont incomplets. C'est dommage, le principe de listing est finalement très similaire aux autres fonctions. Inspires-toi du correctif pour tes prochains exercices. 
- Les requêtes ne sont pas correctes ; tu ajoutes des "{" et des "}". Si le prénom est "Henry", ça donne donc : " firstname='{henry}' "
- Les modèles sont clairement incomplets.

## CONTROLLER ##
- Initiation d'un objet sans vérification des erreurs. Il n'est finalement pas insérer, mais c'est logiquement dommage de commencer une action qui ne sera pas terminée. Il vaut mieux débuter les "set" uniquement lorsque tu es certain qu'il ne comporte rien de faux. 
- Une fonction "studentAdd" est utilisée dans le controller de Teacher sans que cela soit intéressant. C'est une copie de la fonction dans Student.php. "newStudent" n'est pas déclaré. Le controller "Teacher" n'est pas utilisable et n'est pas logique. Dans le cas présent, il est important de pouvoir ajouter un professeur à partir de ce controller (et pas un élève). 

## VIEWS ## 
- Aucune view ne permet actuellement d'effectuer une édition. N'hésites pas à la débuter même si tu n'as pas terminé le code côté controller. Il est parfois avantageux de prendre le problème à l'envers (commencer par la view et remontrer au controller pour se faire une idée des étapes à suivre).
- Aucune view de connexion ; étape très importante du projet. 
- Le principe des views n'est pas compris. Le principe d'une vue de ce projet n'est pas d'être redondant mais de ne modifier que ce qui va changer dans ta page ; une partie du HTML dans le body. En ne modifiant que cette partie, on évite donc de prendre le risque de se répéter, de se tromper et surtout ; on va simplifier la maintenance. Dans ton modèle actuel, si on devait ajouter quelque chose dans le HEAD, on devrait le faire dans chaque fichier html.


Un peu d'effort, tu dois renforcer tes connaissances et passer plus de temps sur tes projets.
N'hésites surtout pas à t'inspirer du correctif pour t'améliorer et faire mieux la prochaine fois.
Il pourrait être intéressant pour toi de recommencer ce projet. 