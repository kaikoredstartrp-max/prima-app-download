# PRIMA App — Guide testeur famille (V1 privée)

**Statut :** version **V1 privée famille** — usage test interne uniquement.  
**Pas une release publique.** Pas d’accès Precision public. Pas de Fusion Shadow.

---

## En bref

PRIMA App propose un parcours unique **PRIMA Génie** : Soul → VDA → Shadow en une seule expérience.  
Les anciens tests séparés (3 cartes « Disponible ») ne doivent **pas** apparaître.

---

## Prérequis (Windows)

| Outil | Pourquoi |
|--------|----------|
| **Windows 10 ou 11** | Application de bureau |
| **Installateur `PRIMA_App_Setup.exe`** | Installe PRIMA App (raccourcis menu Démarrer / bureau) |

**Aucune installation technique requise** : AutoHotkey v2, Node portable et moteur CJS sont **embarqués** dans le dossier d’installation. Vous n’avez pas à installer Node.js ni AutoHotkey sur votre PC.

Téléchargement : page famille → bouton **Télécharger l’installateur PRIMA**.

---

## Mode officiel V1

Le questionnaire est en mode **Génie** :

- Fichier local : `settings/prima_questionnaire.ini` → `questionnaire=genie`
- Modèle fourni : `settings/prima_questionnaire.ini.example` (copier vers `prima_questionnaire.ini` si besoin)

**Parcours visible :** PRIMA Soul → bouton **PRIMA Génie** uniquement.  
**Résultats :** Soul, VDA et Shadow s’ouvrent **après** le parcours, comme lectures — pas comme 3 tests à lancer séparément.

---

## Lancement

1. Télécharger et lancer **`PRIMA_App_Setup.exe`** (installateur Windows).
2. Ouvrir **PRIMA App** depuis le menu Démarrer ou le raccourci bureau  
   (ou double-clic **`LANCER_PRIMA.bat`** dans le dossier d’installation).
3. Choisir ou **créer un profil** (de préférence un profil neuf pour un test complet).
4. Suivre l’écran d’accueil jusqu’à **Home**.
5. Cliquer sur **PRIMA Soul** (🧭).

---

## Parcours test recommandé

### 1. Hub PRIMA Soul

Vérifier :

- Titre **PRIMA Soul**
- Bouton principal **PRIMA Génie**
- **Générer ma lecture** (avant la fin : message du type *Termine le parcours PRIMA Génie…*)
- **Absence** des cartes : « PRIMA Soul Disponible », « PRIMA VDA Disponible », « PRIMA Shadow Disponible »
- **Absence** de « Disponible après les 3 tests »

### 2. PRIMA Génie

1. Cliquer **PRIMA Génie**
2. **Commencer** le parcours
3. Répondre aux questions (barre de progression Soul / VDA / Shadow)
4. Valider les 3 phases (écrans de transition entre phases)
5. À la fin : **Parcours Génie terminé** → **Générer ma lecture**

**Reprise (optionnel) :** quitter au milieu du parcours, relancer l’app, rouvrir **PRIMA Génie** — la session doit reprendre.

### 3. Lecture finale

Après parcours terminé :

- Hub : **Résultat Soul**, **Résultat VDA**, **Résultat Shadow**, **Générer ma lecture — Prêt**
- Ouvrir chaque résultat et faire défiler la page
- Vérifier la **boussole / radar** et le **classement**

---

## Ce qui est normal (V1)

| Comportement | Explication |
|--------------|-------------|
| **Nombre de questions variable** | Le parcours s’adapte au signal (Soul peut s’arrêter vers Q15, VDA/Shadow selon la clarté). |
| **Radar natif « approximatif »** | Cercle en contrôles Windows (pas une image) — fonctionnel et lisible. |
| **VDA base / phase** | Pas encore différenciés dans tous les textes. |
| **Shadow — émotion principale** | Pas encore mesurée dans ce parcours. |
| **Lecture « provisoire »** | Formulations en pistes, pas un diagnostic médical ou psychologique. |
| **Bannière diag hub** (petit texte GP-B1) | Outil de vérification interne — peut être retirée plus tard. |

---

## Ce qui est un bug (signaler immédiatement)

- **Crash** ou message d’erreur technique (JSON, GDI, exit code, etc.)
- **Cartes legacy** visibles (3 tests séparés « Disponible »)
- **Famille symbolique** ou labels officiels exposés (PCM, péché capital, etc.)
- Impossible de **terminer le parcours** ou d’**ouvrir les résultats**
- **Reprise** qui efface la session sans raison
- Texte **incompréhensible** ou anxiogène pour un testeur non développeur

---

## Données locales (confidentialité)

Tout reste sur votre PC :

- `profiles/` — profils et résultats
- `logs/` — journaux techniques
- `settings/` — préférences session

Ces dossiers ne sont **pas** envoyés sur Internet par PRIMA App.

---

## QA rapide (développeur / pilote — optionnel)

Avant un test famille, le pilote peut exécuter :

```powershell
cd C:\chemin\vers\PRIMA_App_V0_1

& "C:\Program Files\AutoHotkey\v2\AutoHotkey64.exe" /validate "PrimaApp.ahk"
& "C:\Program Files\AutoHotkey\v2\AutoHotkey64.exe" /validate "system\prima_genie_ui.ahk"
& "C:\Program Files\AutoHotkey\v2\AutoHotkey64.exe" "tests\run_genie_bridge_qa_only.ahk"
Get-Content tests\logs\genie_bridge_qa_only.txt
```

Attendu : `pass=38 fail=0`

---

## Hors scope V1 famille

- **Precision** (aperçu public)
- **Fusion Shadow**
- Kit PRIMA / modules non demandés pour ce test
- Publication ou partage du dépôt sans accord

---

## Retour test

Noter : **GO / NO GO** + captures si possible (hub, fin de parcours, un écran résultat).  
Indiquer : profil utilisé, durée approximative, blocage éventuel.

*Dernière base validée : parcours Génie B1.1/B1.2 — commit `941c7e5` et suivants.*
