# Comptage Tables Casino — Projet Android Studio

## Installation Android Studio (si pas déjà fait)
1. Télécharger : https://developer.android.com/studio
2. Installer et lancer Android Studio
3. Au premier démarrage : accepter la licence, installer le SDK Android (automatique)

## Ouvrir le projet
1. Dans Android Studio : File → Open
2. Sélectionner le dossier **casino-android** (ce dossier)
3. Attendre que Gradle synchronise (barre de progression en bas, ~1-2 min)

## Générer l'APK
1. Menu : Build → Build Bundle(s) / APK(s) → **Build APK(s)**
2. Attendre la compilation (~1 min)
3. Une notification apparaît : "APK(s) generated successfully"
4. Cliquer sur **"locate"** dans la notification
5. L'APK se trouve dans : app/build/outputs/apk/debug/app-debug.apk

## Installer sur ton téléphone Android
### Option A — Câble USB
1. Sur ton téléphone : Paramètres → À propos → taper 7 fois sur "Numéro de build"
2. Paramètres → Options développeur → activer "Débogage USB"
3. Dans Android Studio : Run → Run 'app' (icône ▶)

### Option B — Transfert fichier
1. Copier app-debug.apk sur ton téléphone (câble, mail, Drive...)
2. Sur le téléphone : ouvrir le fichier APK
3. Accepter "Installer depuis sources inconnues" si demandé
4. Installer → l'icône "Comptage Tables" apparaît

## Structure du projet
casino-android/
├── app/src/main/
│   ├── assets/index.html        ← L'application complète (modifiable)
│   ├── java/.../MainActivity.java ← WebView plein écran
│   └── AndroidManifest.xml
└── app/build.gradle

## Modifier l'app
Pour toute modification (nouvelle table, formule, couleur...) :
→ Éditer uniquement le fichier assets/index.html
→ Rebuilder l'APK
