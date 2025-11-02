EcoKids – Découverte de la nature
Une application mobile éducative destinée aux enfants, pour leur permettre d’apprendre la nature (animaux, plantes) à travers des jeux interactifs, des quiz personnalisés et des activités ludiques basées sur la reconnaissance d’images.

Ce projet est réalisé dans le cadre d'un projet étudiant.

Fonctionnalités (Périmètre)
L'application est construite autour de 4 modules principaux :

Module Découverte (Learn) : Permet de rechercher et de consulter des fiches descriptives simples sur les animaux et les plantes. (Source : API Vikidia)

Module Quiz (Play) : Propose des quiz à choix multiples, filtrés par thème et par niveau. Les questions sont stockées dans Firebase. (Source : Firebase Firestore)

Reconnaissance IA (Scan) : Utilise la caméra pour identifier un élément naturel (plante/animal) et affiche sa fiche "Découverte". (Source : Google Cloud Vision)

Gestion de Profil : Permet à chaque enfant de s'inscrire et de suivre ses progrès, scores et badges gagnés lors des quiz. (Source : Firebase Auth & Firestore)

Stack Technique
Ce projet utilise une stack moderne pour le développement mobile multi-plateforme.

Développement Mobile : Flutter (Dart)

Backend (BaaS) : Firebase (Authentication, Firestore, Storage)

API Externe : Vikidia API (pour le contenu éducatif "Learn")

Intelligence Artificielle : Google Cloud Vision (pour la reconnaissance d'images)

Gestion d’état : Provider / Riverpod

Architecture : Clean Architecture (Modulaire / "Feature-First")

Démarrage Rapide (Getting Started)
Instructions pour configurer et lancer le projet localement.

1. Prérequis
Flutter SDK (v3.x.x ou plus récent)

Un compte Firebase

Un compte Google Cloud Platform avec l'API "Cloud Vision" activée.

Un éditeur de code (VS Code / Android Studio).

2. Installation et Lancement
Cloner le dépôt

Bash

git clone https://github.com/[VOTRE_NOM_GITHUB]/ecokids-app.git
cd ecokids-app
Installer les dépendances

Bash

flutter pub get
Configurer Firebase

Suivez les instructions pour ajouter Firebase à votre projet Flutter en utilisant la FlutterFire CLI :

```bash
flutterfire configure
```

  * Cela générera automatiquement votre fichier `firebase_options.dart`.
Configurer les Clés API

Créez un fichier pour vos clés API (ex: lib/core/config/api_keys.dart - N'oubliez pas d'ajouter ce fichier à votre .gitignore !)

```dart
// lib/core/config/api_keys.dart
class ApiKeys {
  static const String googleVisionApiKey = 'VOTRE_CLE_API_VISION_ICI';
}
```
Lancer l'application

Bash

flutter run
Structure du Projet
Nous utilisons une architecture "Feature-First". Le code est séparé par modules, et chaque module possède sa propre structure data, domain et presentation.

ecokids-app/
│
├── lib/
│   │
│   ├── core/      # Code partagé (Auth, Thème, Erreurs, Widgets communs)
│   │   ├── auth/
│   │   ├── config/
│   │   ├── error/
│   │   └── widgets/
│   │
│   ├── features/  # Modules spécifiques de l'application
│   │   ├── 01_quiz_play/
│   │   ├── 02_decouverte_learn/
│   │   └── 03_vision_ia/
│   │
│   └── main.dart  # Point d'entrée
│
└── pubspec.yaml
