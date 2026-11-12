# .github

[![Visibilité publique](https://img.shields.io/badge/visibilit%C3%A9-publique-blue)](https://docs.github.com/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)
[![Formulaires d'issue](https://img.shields.io/badge/formulaires_d%27issue-4-lightgrey?logo=github)](.github/ISSUE_TEMPLATE)
[![Licence propriétaire](https://img.shields.io/badge/licence-propri%C3%A9taire-lightgrey)](#licence)

Fichiers communautaires par défaut de l'organisation Le Loup Production. GitHub les applique à tous les dépôts de l'organisation, privés compris, qui n'ont pas les leurs.

## Fonctionnalités

À l'ouverture d'une issue, dans n'importe quel dépôt de l'organisation, GitHub propose quatre formulaires au lieu d'une issue vide :

| Formulaire | Type d'issue | Ce qu'il demande |
|---|---|---|
| Signaler un bug | `Bug` | Partie concernée, version, système et machine, gravité, fréquence, constat, attendu, étapes pour reproduire, date et heure, installation en place, journaux (avec leur emplacement par système), captures |
| Problème de connexion réseau | `Bug` | Symptôme, postes avec rôle et IP, écran « Diagnostic réseau », état de la connexion Companion, type de réseau, profil réseau Windows, pare-feu, essais déjà faits, journaux |
| Proposer une fonctionnalité | `Feature` | Besoin en régie, solution imaginée, contournement actuel, utilisateurs et moment d'usage, priorité, échéance, maquettes |
| Tâche technique | `Task` | Objectif, critères de fin, pistes techniques, dépendances |

Les issues vides sont désactivées pour les rôles Read et Triage. Les formulaires de bug demandent de confirmer qu'aucun mot de passe, jeton ou clé ne figure dans le signalement.

## Prérequis

- Le dépôt doit rester **public** et s'appeler `.github` : GitHub ne lit les fichiers par défaut d'une organisation que depuis ce dépôt.
- Les types d'issue `Bug`, `Feature` et `Task` existent au niveau de l'organisation (Settings → Planning → Issue types). Les formulaires n'utilisent pas de labels, qui seraient à créer dans chaque dépôt.

## Contenu

| Chemin | Rôle |
|---|---|
| `.github/ISSUE_TEMPLATE/1-bug.yml` | Formulaire « Signaler un bug » |
| `.github/ISSUE_TEMPLATE/2-reseau.yml` | Formulaire « Problème de connexion réseau » |
| `.github/ISSUE_TEMPLATE/3-fonctionnalite.yml` | Formulaire « Proposer une fonctionnalité » |
| `.github/ISSUE_TEMPLATE/4-tache.yml` | Formulaire « Tâche technique » |
| `.github/ISSUE_TEMPLATE/config.yml` | Issues vides désactivées, lien vers la vue d'ensemble de l'organisation |

Le préfixe numérique fixe l'ordre d'affichage dans le sélecteur.

## Utilisation

Sur un dépôt de l'organisation : **Issues → New issue**, puis choisir le formulaire. Un dépôt qui a son propre dossier `.github/ISSUE_TEMPLATE` n'hérite d'**aucun** de ces formulaires : ne pas en créer dans les dépôts de la suite.

## Limites

- GitHub n'impose les champs obligatoires (`required`) que dans les dépôts publics. Dans les dépôts privés, ils sont affichés mais un formulaire incomplet peut être envoyé : relire les signalements et demander ce qui manque.
- Rien de confidentiel dans ce dépôt : il est visible de tous. Les textes restent génériques (pas de ports, d'adresses ni de noms de postes).

## Développement

Syntaxe des formulaires : [issue forms](https://docs.github.com/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-issue-forms) et [schéma des formulaires](https://docs.github.com/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-githubs-form-schema). Un formulaire invalide n'apparaît pas dans le sélecteur : après une modification, ouvrir **New issue** sur un dépôt de l'organisation et vérifier chaque formulaire. Les `id` de champ servent au pré-remplissage par URL (`?template=1-bug.yml&version=0.4.0`) : ne pas les renommer sans raison.

## Licence

Propriétaire, Le Loup Production.
