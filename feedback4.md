Bonjour,

Je remarque que tu as essayé de compléter le projet et d'atteindre la fin de ce dernier. Malheureusement, je pense que tu as codé à l'aveugle sans tester durant ton avancement. Les erreurs sont nombreuses et rendent ton projet malheureusement inutilisable.

## ROUTES ##
- Aucune redirection en arrivant sur le site, il est donc difficile de le tester. 
- Une erreur bloque effectivement ton travail. C'est dommage.
- Les routes ne sont pas présentes dans tes fichiers. Un fichier adéquat t'aiderait à les configurer et à les rendre plus compréhensibles.

## REMARQUES MODEL ##
- Il est plus simple d'utiliser self::class au lieu de spécifier le nom du model utilisé. Cela pourrait éviter des erreurs  😅
- Les requêtes ne sont pas correctes ; tu ajoutes des "{" et des "}". Si le prénom est "Henry", ça donne donc : " firstname='{henry}' "
- Les modèles sont clairement incomplets.
- De nombreux manquements ; add, update, ... Les models sont incomplets. C'est dommage, le principe de listing est finalement très similaire aux autres fonctions. Inspires-toi du correctif pour tes prochains exercices. 

## CONTROLLER ##
- Déclaration d'un modèle ; L'initialisaton n'est pas bonne :
        $teachersModel = new Teachers
        teachers();
  C'est bien plus simple que cela : 
        $teachersModel = new Teachers();
Même chose pour le controller student
- Manque du controller "ErrorController" = erreur au démarrage du projet 
- Il manque de nombreux fichiers fournis au début du projet dont des fichiers de configuration. C'est vraiment dommage 😅

## VIEWS ## 
- Le layout header n'est pas présent. 


J'ai l'impression qu'il y a eu une petite erreur lors de la récupération du projet sur git. Les parties à développer sont bien là, mais il manque des fichiers pourtant dans le projet de base. 
Je ne peux que te conseiller de bien regarder ton historique Git et/ou de vérifier que tu n'as pas fait une petite erreur de dernière minute ! ;) 