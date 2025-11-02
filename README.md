# EcoKids – Découverte de la nature

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-blue.svg)

Une application mobile éducative destinée aux enfants, pour leur permettre d’apprendre la nature (animaux, plantes) à travers des jeux interactifs, des quiz personnalisés et des activités ludiques basées sur la reconnaissance d’images.

*Ce projet est réalisé dans le cadre d'un projet étudiant.*

## Fonctionnalités (Périmètre)

L'application est construite autour de 4 modules principaux :

* **Module Découverte (Learn)** : Permet de rechercher et de consulter des fiches descriptives simples sur les animaux et les plantes. (Source : API Vikidia)
* **Module Quiz (Play)** : Propose des quiz à choix multiples, filtrés par thème et par niveau. Les questions sont stockées dans Firebase. (Source : Firebase Firestore)
* **Reconnaissance IA (Scan)** : Utilise la caméra pour identifier un élément naturel (plante/animal) et affiche sa fiche "Découverte". (Source : Google Cloud Vision)
* **Gestion de Profil** : Permet à chaque enfant de s'inscrire et de suivre ses progrès, scores et badges gagnés lors des quiz. (Source : Firebase Auth & Firestore)

---

## Stack Technique

Ce projet utilise une stack moderne pour le développement mobile multi-plateforme.

* **Développement Mobile** : Flutter (Dart)
* **Backend (BaaS)** : Firebase (Authentication, Firestore, Storage)
* **API Externe** : Vikidia API (pour le contenu éducatif "Learn")
* **Intelligence Artificielle** : Google Cloud Vision (pour la reconnaissance d'images)
* **Gestion d’état** : Provider / Riverpod
* **Architecture** : Clean Architecture (Modulaire / "Feature-First")

---

## Démarrage Rapide (Getting Started)

Instructions pour configurer et lancer le projet localement.

### 1. Prérequis

* [Flutter SDK](https://flutter.dev/docs/get-started/install) (v3.x.x ou plus récent)
* Un compte [Firebase](https://firebase.google.com/)
* Un compte [Google Cloud Platform](https://cloud.google.com/) avec l'API "Cloud Vision" activée.
* Un éditeur de code (VS Code / Android Studio).

### 2. Installation et Lancement

1.  **Cloner le dépôt**
    ```bash
    git clone [https://github.com/](https://github.com/)[VOTRE_NOM_GITHUB]/ecokids-app.git
    cd ecokids-app
    ```

2.  **Installer les dépendances**
    ```bash
    flutter pub get
    ```

3.  **Configurer Firebase**
    * Suivez les instructions pour ajouter Firebase à votre projet Flutter en utilisant la **FlutterFire CLI** :
    ```bash
    flutterfire configure
    ```
    * Cela générera automatiquement votre fichier `firebase_options.dart`.

4.  **Configurer les Clés API**
    * Créez un fichier pour vos clés API (ex: `lib/core/config/api_keys.dart` - *N'oubliez pas d'ajouter ce fichier à votre `.gitignore` !*)
    ```dart
    // lib/core/config/api_keys.dart
    class ApiKeys {
      static const String googleVisionApiKey = 'VOTRE_CLE_API_VISION_ICI';
    }
    ```

5.  **Lancer l'application**
    ```bash
    flutter run
    ```

---
