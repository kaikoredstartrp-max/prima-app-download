# prima-app-download

Site GitHub Pages pour telecharger **PRIMA App V0.1** (Windows, local-first).

## Contenu du depot

| Fichier | Role |
|---------|------|
| `index.html` | Page d accueil |
| `style.css` | Styles de la page |
| `PRIMA_App_V0_1_Install.zip` | Package d installation propre |

## Installation (utilisateur final)

1. Telechargez `PRIMA_App_V0_1_Install.zip` depuis la page GitHub Pages.
2. Extrayez l archive dans un dossier de votre choix.
3. Installez **[AutoHotkey v2](https://www.autohotkey.com/)** si ce n est pas deja fait (version 2 uniquement).
4. Lancez `launch_prima.ahk` ou le raccourci `PRIMA App.lnk`.
5. Creez un profil et definissez un mot de passe local.
6. Ouvrez **Kit PRIMA** pour verifier que l installation est complete.

## Prerequis

- **Windows**
- **AutoHotkey v2** (obligatoire)

## Local-first

- Toutes les donnees utilisateur sont stockees localement (`profiles/`, `logs/`, `reviews/`).
- Aucune synchronisation cloud automatique.
- Aucun compte ni cle API requis pour utiliser PRIMA App V0.1.

## Donnees incluses dans le zip

Le package contient uniquement :

- `PrimaApp.ahk`, `launch_prima.ahk`, `PRIMA App.lnk` (si genere)
- `README_INSTALLATION.txt`
- Dossiers vides `profiles/`, `logs/`, `reviews/`
- `profiles/profiles.ini` avec section `[Index]` vide

**Non inclus** : profils personnels, logs, reviews, archives, mots de passe, hash/salt, `app_state.ini`.

## GitHub Pages

Ce depot est prevu pour etre publie en **GitHub Pages** depuis la branche `main`, dossier racine (`/`).

### Activer Pages

1. Creez le depot GitHub `prima-app-download` (public).
2. Poussez le contenu de ce dossier sur `main`.
3. Sur GitHub : **Settings -> Pages**
4. **Build and deployment -> Source** : Deploy from a branch
5. **Branch** : `main` -> dossier **/ (root)** -> **Save**
6. Attendez 1-2 minutes ; l URL sera affichee dans Settings -> Pages.

URL attendue : `https://<votre-compte>.github.io/prima-app-download/`

## Mise a jour du zip

Lors d une nouvelle version, remplacez `PRIMA_App_V0_1_Install.zip` dans ce dossier (depuis le build propre du projet PRIMA), verifiez l absence de donnees personnelles, puis committez et poussez.
