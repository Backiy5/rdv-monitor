# RDV Monitor

Ce projet contient une application Android (Kotlin) qui :

- Surveille la page de la préfecture pour les créneaux :  
  https://www.rdv-prefecture.interieur.gouv.fr/rdvpref/reservation/demarche/6880/creneau/
- Cherche le texte **"créneau disponible"**
- Vérifie toutes les 8 minutes
- Envoie une **notification** sur le téléphone si un créneau apparaît

## Instructions pour compiler l'APK

1. Ouvrir le projet dans **Android Studio**
2. Build → Build Bundle(s) / APK(s) → Build APK(s)
3. L’APK se trouve dans :  
   `app/build/outputs/apk/debug/app-debug.apk`

## GitHub Actions

- Un workflow GitHub Actions peut compiler automatiquement l’APK à chaque push
- Voir le fichier `.github/workflows/android.yml`

## Remarques

- Android 8+ impose des restrictions sur les services en arrière-plan. Ce projet utilise un service foreground.
- Respectez les conditions d’utilisation du site officiel.
