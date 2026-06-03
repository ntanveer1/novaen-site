# /commit

> Commande pour sauvegarder l'état du workspace avec Git.

---

## Mission

Quand je lance `/commit`, exécute la séquence suivante :

### Étape 1 : Vérifier que Git est initialisé

Vérifie si un dépôt Git existe à la racine du workspace (présence d'un dossier `.git`).

- **Si non** : initialise Git avec `git init`, puis continue.
- **Si oui** : continue directement.

### Étape 2 : Analyser les changements

Lance `git status` pour voir ce qui a changé depuis le dernier commit (ou depuis le début si c'est le premier commit).

Présente-moi un résumé lisible des fichiers modifiés, ajoutés ou supprimés. Regroupe-les par catégorie si c'est utile (contexte, livrables, commandes, config...).

### Étape 3 : Proposer un message de commit

Génère un message de commit clair et descriptif en français, qui résume ce qui a changé. Format :

```
[type] résumé court des changements

- détail 1
- détail 2
```

Types possibles : `init`, `contexte`, `livrable`, `config`, `commande`, `mix`

Exemples :
- `init : mise en place du workspace Jarvis`
- `contexte : mise à jour des objectifs et nouveaux projets`
- `livrable : ajout landing page NOVAËN`
- `config : ajout .gitignore et gestion des secrets`

Propose le message et attends ma confirmation avant de commiter.

### Étape 4 : Commiter

Une fois que j'ai confirmé (ou modifié) le message :

1. Stage tous les fichiers non ignorés : `git add .`
2. Crée le commit avec le message validé
3. Affiche la confirmation : hash du commit, nombre de fichiers, message

---

## Règles importantes

- Ne jamais stager `.env` (vérifie que `.gitignore` est bien en place avant de faire `git add .`)
- Si `.gitignore` est absent, le signaler et stopper avant de stager quoi que ce soit
- Toujours demander confirmation sur le message avant de commiter
- Si aucun changement n'est détecté, le dire clairement et ne rien faire
- Réponses en français, pas de tirets longs (em dashes)
