# strategie_securisation_filRouge
Stratégie de Conception et de Sécurisation du Projet Fil Rouge


**Introduction**

In the digital age, ensuring the security and integrity of user data is paramount for any web
application. This document describes the security strategy for the RMS application, aimed at
protecting user data and maintaining trust.


## Table des matières

1. [Introduction à la Sécurité de l'Application](https://github.com/Jwell2014/strategie_securisation_filRouge/blob/master/Introduction_Securite_Application)
   1. [Analyse des Risques](https://github.com/Jwell2014/strategie_securisation_filRouge/blob/master/Introduction_Securite_Application/Analyse_Risques.md)
   2. [Objectifs de Sécurité](https://github.com/Jwell2014/strategie_securisation_filRouge/blob/master/Introduction_Securite_Application/Objectifs_Sécurite.md)

2. [Sécurité RMS FRONT-END](https://github.com/Jwell2014/strategie_securisation_filRouge/blob/master/Front)
    1. [Authentification Robuste](https://github.com/Jwell2014/strategie_securisation_filRouge/blob/master/Front/Authentification_robuste.md)
    2. [Validation des Entrées Utilisateur](https://github.com/Jwell2014/strategie_securisation_filRouge/blob/master/Front/Validation_entree_utilisateur.md)
    3. [Exigences RGPD](https://github.com/Jwell2014/strategie_securisation_filRouge/blob/master/Front/RGPD.md)

2. [Sécurité RMS BACK-END](https://github.com/Jwell2014/strategie_securisation_filRouge/blob/master/Back)
    1. [Authentification Robuste](https://github.com/Jwell2014/strategie_securisation_filRouge/blob/master/Back/Authentification_robuste.md)
    2. [Gestion des Autorisations (RBAC)](https://github.com/Jwell2014/strategie_securisation_filRouge/blob/master/Back/Gestion_Autorisations_(RBAC).md)
    3. [Protection contre les Injections SQL](https://github.com/Jwell2014/strategie_securisation_filRouge/blob/master/Back/Protection_injection_SQL.md)  
    4. [Validation des Entrées Utilisateur](https://github.com/Jwell2014/strategie_securisation_filRouge/blob/master/Back/Validation_entree_utilisateur.md)  
    5. [Utilisation d'un ORM (Object-Relational Mapping)](https://github.com/Jwell2014/strategie_securisation_filRouge/blob/master/Back/ORM.md)  


2. [Sécurité RMS BDD](https://github.com/Jwell2014/strategie_securisation_filRouge/blob/master/BDD)
    1. [Chiffrement des Données Sensibles](https://github.com/Jwell2014/strategie_securisation_filRouge/blob/master/BDD/Chiffrement_donnee_sensibles.md)
    2. [Gestion des Mots de Passe](https://github.com/Jwell2014/strategie_securisation_filRouge/blob/master/BDD/Gestion_MDP.md)
    3. [Protection contre les Attaques par Déni de Service (DoS)](https://github.com/Jwell2014/strategie_securisation_filRouge/blob/master/BDD/Protection_attaque_dos.md)

# Projet

Votre mission est de présenter une stratégie de sécurisation de votre applications web, en appliquant cette stratégie sur la conception de votre projet fil rouge.

## Contexte du projet

Vous êtes sur le point de commencer la conception de votre application Fil Rouge, c'est le meilleur moment pour effectuer une recherche de documentation / veille et de déterminer une stratégie de sécurisation de votre application.

​

Dans ce brief, vous allez devoir effectuer des recherches, analyser les risques et les enjeux de sécurité pour garantir l'intégrité des données que vos futurs utilisateurs vous confieront par le bias de votre application.

​

Et appliquer cette strategie sur votre conception de votre projet Fil rouge.

# Modalités pédagogiques

Rendu individuel, présentation en groupe :
* Livraison Vendredi 05 Avril à 22h (premiere partie pour ECF).
* Présentation libre dans le format mais impérativement basé sur un support visuel.

# Modalités d'évaluation

* Présentation devant un jury
* Analyse de la stratégie de sécurité proposée
* Questions / Réponses

# Livrables

* Un document PDF contenant toute la stratégie choisie (ressources incluses en annexe).

# Critères de performance

* L'introduction doit être en anglais
* La présentation doit être pédagogique et facile à comprendre pour un néophyte
* Les informations doivent être techniquement justes et tirées de sources "fiables" et/ou officielles (ANSSI, OWASP, MDN, Stackoverflow, etc...)
* La stratégie de sécurisation doit couvrir tout le cycle de vie du développement de votre application
* La stratégie de sécurisation doit couvrir toutes les couches metiers de l'application
