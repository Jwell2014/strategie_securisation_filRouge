# 2.2. Gestion des Autorisations dans l'Application avec RBAC 

Dans le cadre de notre application, la gestion des autorisations est un élément crucial pour
garantir un accès sécurisé aux fonctionnalités et aux données. Pour cela, nous avons adopté le
modèle de Contrôle d'Accès Basé sur les Rôles (RBAC), qui définit les autorisations en fonction
des rôles des utilisateurs.

**Les Rôles** :

Admin : Les administrateurs bénéficient du plus haut niveau d'accès dans l'application. Ils ont le
privilège d'accéder à toutes les fonctionnalités et à toutes les données, ce qui leur permet de
superviser et de gérer l'ensemble de l'application, y compris les fonctionnalités avancées.

Client : Les clients sont les utilisateurs standard de l'application. Leur accès est limité aux
fonctionnalités et aux données nécessaires à leur utilisation prévue de l'application, comme la
gestion des données personnelles et la visualisation d'informations pertinentes.

Dev : Les développeurs sont des utilisateurs internes, souvent impliqués dans le développement
et la maintenance de l'application. Ils ont accès à des fonctionnalités spécifiques et à des
données sensibles liées au développement et à la gestion de l'application.

**Le Contrôle d'Accès** :

Nous avons mis en place une logique de contrôle d'accès qui vérifie le rôle de l'utilisateur et la
ressource demandée pour déterminer s'il est autorisé à y accéder.
Par exemple :

Les administrateurs ont un accès complet à toutes les fonctionnalités et à toutes les
données.
Les clients ont un accès restreint conformément à leur rôle dans l'application.
Les développeurs ont un accès spécialisé aux fonctionnalités et aux données liées au
développement.

Parallèlement à cela, nous utilisons Cross-Origin Resource Sharing (CORS) pour gérer les
autorisations d'accès aux ressources entre différentes origines. CORS est un mécanisme de
sécurité qui permet à un site Web d'accéder aux ressources d'un autre site Web, tout en
garantissant que seuls les sites Web autorisés peuvent accéder aux ressources. Cela renforce la
sécurité en limitant les risques liés aux accès non autorisés aux ressources entre différentes
origines.

Grâce à l'utilisation combinée du modèle RBAC et de CORS, nous assurons un accès sécurisé et
approprié à notre application, tout en garantissant la confidentialité et l'intégrité des données.

![Getting Started](/Assets/rbac.png)