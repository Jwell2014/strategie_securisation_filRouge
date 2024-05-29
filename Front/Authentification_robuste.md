### 2.1 Authentification Robuste


Dans le cadre de l'application RMS, l'authentification des utilisateurs est une étape cruciale pour
garantir l'accès sécurisé à la plateforme. Pour répondre à cette exigence, j’utilise JSON Web
Tokens (JWT) comme méthode d'authentification robuste, en tenant compte de la Same Origin
Policy (SOP).

La Same Origin Policy est un mécanisme de sécurité intégré dans les navigateurs Web qui
impose des restrictions sur l'accès aux ressources entre différentes origines. Cela signifie que,
par défaut, les ressources telles que les cookies ou les données stockées localement par le
navigateur ne peuvent être partagées qu'entre des pages du même domaine, du même
protocole et du même port. Cette politique empêche les attaques telles que les fuites
d'informations et les atteintes à la confidentialité en limitant l'accès des scripts aux données des
autres origines.

Dans le contexte de l'authentification basée sur JWT, la SOP garantit que les JWT émis par le
serveur ne peuvent être lus que par le client de l'application RMS. Cela empêche les attaquants
d'intercepter et de manipuler les jetons d'authentification entre les différents domaines,
renforçant ainsi la sécurité de l'authentification des utilisateurs.

En intégrant une authentification robuste basée sur JWT et en tenant compte de la Same Origin
Policy, l'application RMS garantit un accès sécurisé et fiable pour ses utilisateurs, tout en
minimisant les risques d'accès non autorisés et d'atteintes à la confidentialité des données.


**Mécanisme :**

- Utilisation de JSON Web Tokens (JWT) pour l'authentification.
- Stockage sécurisé des JWT dans le stockage local du navigateur.

```Java
// Stocker le JWT après l'authentification
localStorage.setItem('jwt', token);

// Ajouter le JWT à l'en-tête Authorization pour les appels API
fetch('/api/resource', {
  method: 'GET',
  headers: {
    'Authorization': `Bearer ${localStorage.getItem('jwt')}`
  }
});
```