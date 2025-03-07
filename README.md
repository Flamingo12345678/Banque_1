# Banque_1
Application bancaire mobile développée avec SwiftUI pour iOS/iPadOS, offrant une expérience utilisateur fluide et sécurisée pour la gestion des comptes bancaires.

## Présentation du projet

BanqueApp est une application bancaire moderne qui permet aux utilisateurs de gérer leurs finances personnelles depuis leur appareil iOS. Conçue avec SwiftUI, elle offre une interface utilisateur intuitive et réactive tout en garantissant la sécurité des données financières.

## Architecture

L'application suit une architecture MVVM (Model-View-ViewModel) avec une séparation claire des responsabilités :

```
Banque_1/
├── App/                    # Fichiers principaux de l'application
│   ├── Banque_1App.swift  # Point d'entrée de l'application
│   └── ContentView.swift   # Vue principale de navigation
├── Models/                 # Modèles de données
│   ├── MockUser.swift      # Modèle utilisateur pour le développement
│   ├── Transaction.swift   # Modèle de transaction
│   └── MockAppState.swift  # État global de l'application
├── Views/                  # Vues de l'interface utilisateur
│   ├── LoginView.swift     # Écran de connexion
│   ├── DashboardView.swift # Tableau de bord principal
│   └── ...                 # Autres vues
├── Services/               # Services et APIs
│   ├── MockAPIService.swift # Service API simulé
│   ├── PersistenceController.swift # Gestion de CoreData
│   ├── ErrorHandler.swift  # Gestionnaire d'erreurs centralisé
│   └── Logger.swift        # Système de journalisation
├── Config/                 # Configuration
│   └── EnvironmentManager.swift # Gestionnaire d'environnements
└── Resources/              # Ressources
    ├── en.lproj/          # Localisation anglaise
    └── fr.lproj/          # Localisation française
```

## Fonctionnalités principales

### Authentification
- Connexion sécurisée avec un numéro de compte et mot de passe
- Support pour l'authentification biométrique (Touch ID/Face ID)
- Gestion des sessions avec expiration automatique

### Gestion des comptes
- Consultation du solde en temps réel
- Historique détaillé des transactions
- Filtrage et recherche des opérations

### Opérations bancaires
- Virements entre comptes
- Dépôts et retraits
- Paiements programmés

### Profil utilisateur
- Gestion des informations personnelles
- Préférences de notification
- Paramètres de sécurité

## Technologies utilisées

- **SwiftUI**: Framework d'interface utilisateur déclaratif d'Apple
- **Combine**: Pour la programmation réactive et la gestion des états
- **CoreData**: Persistance des données locales
- **OSLog**: Journalisation structurée des événements
- **XCTest**: Tests unitaires et d'interface

## Gestion des environnements

L'application dispose de plusieurs environnements configurables pour faciliter le développement et les tests :

### Développement
- Utilise des services simulés (MockAPIService)
- Données de test prédéfinies
- Journalisation détaillée
- Outils de débogage activés

### Pré-production (Staging)
- Connecté à l'API de staging
- Données de test sur le serveur
- Validation des fonctionnalités avant production

### Production
- Environnement de production complet
- Données réelles des utilisateurs
- Optimisations de performance activées

## Gestion des erreurs

Un système centralisé de gestion des erreurs a été implémenté pour :
- Capturer et journaliser toutes les erreurs
- Présenter des messages d'erreur adaptés aux utilisateurs
- Envoyer des rapports d'erreur en production
- Faciliter le débogage en développement

## Internationalisation

L'application prend en charge plusieurs langues :
- Français (langue par défaut)
- Anglais
- Structure en place pour ajouter facilement d'autres langues

## Sécurité

- Chiffrement des données sensibles
- Protection contre les injections SQL
- Validation des entrées utilisateur
- Expiration automatique des sessions
- Conformité aux normes bancaires de sécurité

## Tests

### Tests unitaires
- Tests des modèles de données
- Tests des services et API
- Tests des ViewModels

### Tests d'interface
- Tests des flux utilisateur principaux
- Tests de performance
- Tests d'accessibilité

## Mode développement

En mode développement, l'application offre :
- Un utilisateur de test préconfiguré
- Des transactions simulées
- Un sélecteur d'environnement accessible depuis l'interface
- Des journaux détaillés pour le débogage

## Prérequis pour le développement

- Xcode 14.0 ou supérieur
- iOS 16.0 ou supérieur (cible de déploiement)
- Swift 5.7 ou supérieur
- Compte développeur Apple (pour le déploiement)

## Installation et configuration

1. Cloner le dépôt :
```bash
git clone https://github.com/username/BanqueApp.git
cd Banque_1
```

2. Ouvrir le projet dans Xcode :
```bash
open Banque_1.xcodeproj
```

3. Configurer les environnements dans `Config/EnvironmentManager.swift`

4. Compiler et exécuter l'application sur un simulateur ou un appareil

## Bonnes pratiques implémentées

- **Clean Code** : Code lisible et bien structuré
- **SOLID** : Principes de conception orientée objet
- **DRY** : Éviter la duplication de code
- **Dependency Injection** : Pour faciliter les tests
- **Logging structuré** : Pour un débogage efficace
- **Gestion des erreurs robuste** : Pour une meilleure expérience utilisateur

## Roadmap

### Version 1.1
- Ajout de graphiques pour visualiser les dépenses
- Support pour les notifications push
- Amélioration de l'accessibilité

### Version 1.2
- Intégration avec Apple Pay
- Support pour les comptes multiples
- Catégorisation automatique des transactions

### Version 2.0
- Refonte de l'interface utilisateur
- Support pour les investissements
- Analyse prédictive des dépenses

## Contribution

1. Forker le projet
2. Créer une branche pour votre fonctionnalité (`git checkout -b feature/amazing-feature`)
3. Commiter vos changements (`git commit -m 'Add some amazing feature'`)
4. Pousser vers la branche (`git push origin feature/amazing-feature`)
5. Ouvrir une Pull Request

## Licence

Copyright © 2025 Banque_1. Tous droits réservés.

## Contact

Ernest Evrard Yombi - ernestyombi20@gmail.com
