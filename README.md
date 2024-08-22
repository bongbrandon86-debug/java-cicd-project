# TEST LEAD INTEGRATEUR

# Contexte

Vous travaillez pour une entreprise qui développe une application Java basée sur Maven. L'application doit être construite, testée et déployée automatiquement à chaque commit sur GitLab. Vous devez également intégrer des vérifications de sécurité dans le pipeline CI/CD.

[lien vers le projet gitlab](https://gitlab.com/fodoup/test-integrateur.git)

## Étapes

### 1. Mise en place du Pipeline CI/CD

- Configurez un pipeline CI/CD dans le fichier `.gitlab-ci.yml` qui exécute les étapes suivantes :\
      - **Build** : Construire l'application avec Maven.\
      - **Test** : Exécuter les tests unitaires.\
      - **Analyse de Code** : Intégrer SonarQube pour l'analyse de qualité du code.\
      - **Analyse de Sécurité** : Intégrer une analyse de sécurité (par exemple, OWASP Dependency Check ou Snyk).\
      - **Package** : Générer un package de l'application.\
      - **Déploiement** : Déployer l'application sur un environnement staging (utiliser un Docker container ou une machine virtuelle par exemple).\

- Assurez-vous que les variables sensibles (ex. : clés API, mots de passe) sont gérées de manière sécurisée via les GitLab CI/CD variables.

### 2. Mise en place d'une Stratégie de Déploiement

- Implémentez une stratégie de déploiement sécurisé, par exemple :\
      - **Déploiement Blue-Green**\
      - **Rolling Deployment**

### 3. Surveillance et Notifications

- Configurez des notifications GitLab pour informer l'équipe en cas de succès ou d'échec du pipeline.
- Mettez en place une surveillance basique sur l'environnement staging (par exemple, une vérification de la disponibilité de l'application après déploiement).

## Bonus (Optionnel)

- Ajouter une étape de déploiement en production après validation manuelle.
- Mettre en place un système de backup et rollback en cas d’échec en production.

## Livrables

- Le fichier `.gitlab-ci.yml` complet.
- Un document expliquant la stratégie DevSecOps mise en place, les choix techniques, et les outils utilisés.
