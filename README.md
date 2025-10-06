# Story - Hero's Journey (Projet Git)

Projet collaboratif d'écriture **en branches Git** basé sur le schéma du **Monomythe (Hero’s Journey)**.

## Règles essentielles
- **9 chapitres**, chacun découpé en **12 sections**.
- **1 section = 1 commit** (max **2 phrases**).
- **Ordre d'écriture immuable** dans chaque trio de sections : **Héros → Villain → Helper**.
- Travail **dans des branches courtes** (1 section) puis **merge** régulier dans la **branche du chapitre** toutes les 3 sections (après un trio complet).
- Fin de chapitre : **squash & merge** vers `main`, puis on passe au chapitre suivant.
- **Retours en arrière** autorisés au fil des chapitres selon les rôles (corruption / renforcement / prophétie).

## Chapitres (Hero’s Journey)
- 01 — Call to Adventure
- 02 — Supernatural Aid
- 03 — Threshold
- 04 — Trials
- 05 — Abyss
- 06 — Revelation
- 07 — Atonement
- 08 — Return
- 09 — Gift

## Démarrage rapide
```bash
git init
git checkout -b main
echo "# Story - Hero's Journey" > README.md
git add .
git commit -m "init: repo"

# Chapitre 1
git checkout -b chapter/01-call-to-adventure main

# SECTION 1 (Héros)
git checkout -b feat/hero/c01-s01 chapter/01-call-to-adventure
echo "Héros — Section 1 (≤ 2 phrases)." >> chapters/chapter01.md
git add chapters/chapter01.md
git commit -m "hero(c01 s01): …"
git checkout chapter/01-call-to-adventure
git merge --no-ff feat/hero/c01-s01 -m "merge: hero c01 s01"
```

## Nommage recommandé
- Branches de chapitre : `chapter/01-call-to-adventure`, `chapter/02-supernatural-aid`, …
- Branches de section & rôle : `feat/hero/c01-s01`, `feat/villain/c01-s02`, `feat/helper/c01-s03`.
- Message de commit : `hero(c05 s07): phrase clé`.

## Outils conseillés
- **Git** (CLI) + **GitHub** (ou GitLab/Bitbucket) pour l’hébergement.
- **VS Code** avec **GitLens**, **Markdown All in One**, **Prettier**.
- **GitHub Desktop** (ou **Sourcetree**, **GitKraken**) si vous préférez un GUI.
- Communication: **Teams/Slack**, réunion courte après chaque trio de sections.
