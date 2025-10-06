# Règles du jeu d'écriture

## Structure
- 9 chapitres × 12 sections.
- 1 section = 1 commit (≤ 2 phrases).
- Ordre **Héros → Villain → Helper** pour chaque trio (sections 1–3, 4–6, 7–9, 10–12).

## Workflow Git
1. Créez une **branche de chapitre** depuis `main`: `chapter/<num>-<slug>`.
2. Pour chaque section, créez une **branche courte** `feat/<role>/c<num>-s<section>`.
3. Écrivez la section, committez, puis **merge** dans la branche de chapitre.
4. Après 12 sections, **squash & merge** dans `main`.

## Conflits & Qualité
- En cas de conflit non satisfaisant : `git merge --abort`, **re-squash** la petite branche, réécrivez, puis re-mergez.
- Relisez orthographe/style. Gardez des commits courts et explicites.

## Retours en arrière (selon rôle)
- Héros (dès **Threshold**, chap. 3) peut réviser chap. 1–2 (signes de corruption).
- Villain (au **Abyss**, chap. 5) peut renforcer chap. 1.
- Helper (à **Atonement**, chap. 7) peut ajuster des passages pour accomplir la prophétie.