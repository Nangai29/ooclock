Salut ------,

**Retours concernant l'exercice**

Concernant ton MCD, j'ai quelques petites choses à te remonter : 

- Un utilisateur doit pouvoir liker plusieurs produits & un produit doit pouvoir être aimé par plusieurs utilisateurs. Je pense qu'il y a certaines choses à revoir à ce niveau.

- Le fait de mettre le total de la commande dans "ORDER" n'est ni mauvais ni bon, mais tu dois réfléchir au suivi du prix des produits. Le prix d'un produit peut avoir changé entre la commande et maintenant, il n'y aura donc pas de suivi exact.

- Tu peux pousser le sujet en utilisant des tables d'association (au niveau du contain). De cette façon, tu pourras stocker le prix du produit au moment de l'achat

- Concernant l'adresse, je comprends le choix fait. Il aurait été aussi possible d'utiliser un service permettant de récupérer les adresses françaises et dans un tel cas, une adresse n'aurait pas forcément été liée à une seule personne. 

- Certains verbes sont discutables : GENERATE 

Globalement, le sujet semble être maîtrisé, mais je ne peux que te conseiller d'approfondir avec les tables d'association, tu remarqueras que tu peux potentiellement aller plus loin.


**Outils à utiliser**

J'en profite pour te partager trois outils gratuits pour créer des MCD rapidement et facilement : 

- Draw.io : C'est un outil en ligne gratuit pour la création de diagrammes et de modèles, y compris les MCD. Il offre des modèles pré-conçus et des formes pour faciliter la création de MCD professionnels.

- Lucidchart : C'est un autre outil en ligne gratuit pour la création de diagrammes, y compris les MCD. Il propose des fonctionnalités de collaboration en temps réel, ce qui en fait un excellent choix pour les équipes.

- MySQL Workbench : Il permet de créer des MCD pour les bases de données MySQL. Il offre des fonctionnalités avancées telles que la génération de scripts SQL et la modélisation inverse à partir d'une base de données existante.

Ces trois outils sont largement utilisés et peuvent vous aider à créer des MCD de manière professionnelle et efficace.

Je te souhaite une bonne journée ;)