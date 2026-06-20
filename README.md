# prima-app-download

Site GitHub Pages — **PRIMA App V0.1 — test famille privé** (Génie · banque source-driven multi · choix multiples).

**Ne pas partager le lien publiquement.** Usage cercle proche uniquement.

## Téléchargement

- **Page :** https://kaikoredstartrp-max.github.io/prima-app-download/
- **Installateur :** [PRIMA_App_Setup.exe](PRIMA_App_Setup.exe)
- **ZIP portable :** [PRIMA_App_V0_1_Family.zip](PRIMA_App_V0_1_Family.zip)

## Contenu package validé

- `settings/prima_questionnaire.ini` → mode genie + bank multi
- `prima-soul-engine/output/genie_bank_v2_merged_source_driven_multi.json`
- Aucun profil utilisateur · aucune donnée personnelle

## Prérequis testeur

- Windows 10 ou 11
- Node.js + npx (moteur PRIMA Génie)
- AutoHotkey v2 **non** requis

## Parcours

PRIMA Soul → **PRIMA Génie** (multi-choix, compteur visible) → lecture symbolique après complétion.

## Déploiement (opérateur)

```bat
tools\build_family_package.bat
```

Puis copier `PRIMA_Download_Package\out\*` vers ce repo, mettre à jour `index.html`, `git push`.

Package SHA256 (ZIP) : voir commit message de release.
