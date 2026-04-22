# Lithium Marketing — Dev Standards

Procédure officielle de démarrage de projet chez Lithium Marketing. Ce dépôt héberge le guide HTML interne qui standardise l'initialisation de tout projet ERP ou application web de l'équipe.

**Guide en ligne : [lithium-marketing.github.io/dev-standards](https://lithium-marketing.github.io/dev-standards/)**

## Contenu du dépôt

| Fichier | Rôle |
| --- | --- |
| `index.html` | Guide complet (procédure, prompt standardisé Claude Code, template `.gitignore`, checklist, dépannage) |
| `.gitignore` | Exclusions locales (IDE, settings Claude locaux) |

## Consulter le guide

### En ligne (recommandé)

Version publiée via GitHub Pages, toujours à jour avec la branche `main` :

> https://lithium-marketing.github.io/dev-standards/

### En local

Ouvrir `index.html` directement dans un navigateur. Le document est autonome : pas de build, pas de dépendance, uniquement des polices Google Fonts chargées en ligne.

```powershell
# Depuis PowerShell, à la racine du dépôt
Start-Process index.html
```

## Public visé

Tout développeur rejoignant un projet Lithium Marketing ou démarrant un nouveau projet pour le compte de l'organisation. La procédure suppose un environnement **Windows / PowerShell** et une authentification GitHub fonctionnelle (GitHub CLI ou PAT).

## Ce que couvre le guide

1. **Prérequis** — Node.js 18+, Git, compte Anthropic avec accès Claude Code, accès à l'org GitHub `lithium-marketing`.
2. **Installation de Claude Code** — installation npm globale et première authentification.
3. **Préparation du projet** — création du dossier local en kebab-case (nouveau projet ou transfert de fichiers existants).
4. **Création du dépôt distant** — dépôt GitHub strictement vide dans l'organisation.
5. **Délégation à Claude Code** — prompt standardisé à copier tel quel, qui demande à Claude d'analyser la stack, créer `.gitignore` / `.env.example` / `CLAUDE.md` / `README.md`, initialiser Git, ajouter le remote, puis pousser sur `main`.
6. **Validation finale** — checks Git, structure attendue du projet, format des commits suivants.

Deux sections transverses :

- **Sécurité** — gestion des `.env`, règle d'or `.env` + `.env.example`, marche à suivre si un secret est commité par erreur.
- **Template `.gitignore`** — version de base couvrant Node.js, Python, PHP/Laravel, IDE et OS.

## Mises à jour

Toute amélioration de la procédure passe par une Pull Request sur ce dépôt. Le guide embarque un numéro de version affiché en pied de page (`v1.1 · 2026`) — le mettre à jour en même temps que les changements significatifs.

## Licence

Usage interne Lithium Marketing.
