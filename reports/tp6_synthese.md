# Orchestrateur ou integration continue ? (TP06)

| Critere | Prefect (orchestrateur) | GitHub Actions (CI) |
|---|---|---|
| Ce qui declenche l'execution | Une planification ou un lancement manuel | Un push ou un lancement manuel |
| Ou s'execute le traitement | Sur une machine avec un worker Prefect | Sur un runner GitHub Actions |
| Qui surveille, et ou | Prefect UI : suivi des flows et des tasks | GitHub Actions : suivi des jobs et des steps |
| Ce qui se passe en cas d'echec | Le flow passe en Failed et les retries configurés sont appliqués | Le workflow passe en Failure et affiche l'etape en erreur |
| Type de tache adapte | Orchestration et reentrainement recurrent des modeles | Tests et verification automatique a chaque modification |
| Ce qui est versionne dans Git | Le code du flow et sa configuration | Le code, les scripts et le fichier YAML du workflow |

## Conclusion

Prefect permet de planifier, executer et surveiller les traitements ML.
GitHub Actions permet de verifier automatiquement le pipeline apres chaque modification.
Prefect facilite l'orchestration des workflows.
GitHub Actions garantit le controle de qualite du projet.
Les deux outils sont complementaires et repondent a des besoins differents.