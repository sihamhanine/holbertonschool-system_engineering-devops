this is the readme of the project web infrastructure
0-simple_web_stack
Infrastructure Web Simple
Voici un diagramme de l'infrastructure :

Image du diagramme

Explication :
- Un serveur : Un serveur est un dispositif (physique ou virtuel) ou un programme informatique qui fournit des fonctionnalités à d'autres programmes ou appareils, appelés "clients".

- Le rôle du nom de domaine : Le nom de domaine (comme foobar.com) sert à rendre accessible le serveur par un nom lisible, au lieu d'utiliser une adresse IP (comme 8.8.8.8).

- Le type d'enregistrement DNS www dans www.foobar.com : L'enregistrement www est un enregistrement CNAME ou A record qui mappe un sous-domaine (www) à une adresse IP spécifique du serveur.

- Le rôle du serveur web (Nginx) : Le serveur web reçoit les requêtes HTTP des utilisateurs et renvoie des pages web statiques ou transfère la requête à un serveur d'application pour du contenu dynamique.

- Le rôle du serveur d'application : Le serveur d'application exécute la logique de l'application (comme les calculs, l'accès aux données, etc.) et renvoie la réponse au serveur web.

- Le rôle de la base de données (MySQL) : MySQL stocke les informations nécessaires à l'application (par exemple, les utilisateurs, les produits, etc.) et permet de gérer ces données de manière organisée.

- Le serveur communique avec l'ordinateur de l'utilisateur via : Le serveur communique avec l'utilisateur en utilisant des protocoles réseau comme TCP/IP via HTTP ou HTTPS.

Problèmes avec cette infrastructure :

- SPOF (Single Point of Failure) : Comme il n'y a qu'un seul serveur, si celui-ci tombe en panne, tout le site devient inaccessible.

- Temps d'arrêt pendant la maintenance : Si vous devez redémarrer le serveur web (Nginx) pour déployer du nouveau code, le site sera temporairement hors ligne.

- Pas de scalabilité : Avec une seule machine, le système ne peut pas gérer une augmentation importante du trafic. Il serait nécessaire d'ajouter plus de serveurs pour faire face à une charge importante.