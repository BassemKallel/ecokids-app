# Contribuer à EcoKids

Nous accueillons avec plaisir les contributions pour améliorer EcoKids ! Si vous souhaitez aider, que ce soit pour corriger un bug ou proposer une nouvelle fonctionnalité, voici comment procéder :

## 1. Signaler un Bug ou Proposer une Idée

* Utilisez l'onglet **"Issues"** de ce dépôt GitHub.
* **Pour un bug :** Décrivez le problème précisément, les étapes pour le reproduire, et ce à quoi vous vous attendiez.
* **Pour une fonctionnalité :** Expliquez votre idée et pourquoi elle serait utile à EcoKids.

## 2. Proposer une Modification (Pull Request)

Si vous souhaitez écrire du code, suivez ce processus standard :

1.  **Forkez** le dépôt (cliquez sur le bouton "Fork" en haut à droite).
2.  **Clonez** votre fork sur votre machine locale :
    ```bash
    git clone [https://github.com/](https://github.com/)[VOTRE_NOM_GITHUB]/ecokids-app.git
    ```
3.  Créez une **nouvelle branche** pour votre modification :
    ```bash
    git checkout -b feature/ma-super-feature
    ```
4.  **Codez** votre modification. Assurez-vous de respecter l'architecture "Feature-First" en place.
5.  **Commitez** vos changements avec un message clair :
    ```bash
    git commit -m "feat: Ajout de ma super feature"
    ```
6.  **Pushez** votre branche vers votre fork :
    ```bash
    git push origin feature/ma-super-feature
    ```
7.  Ouvrez une **Pull Request (PR)** depuis votre branche vers la branche `main` (ou `develop`) du dépôt original.
8.  Décrivez ce que fait votre PR et attendez la revue de l'équipe.