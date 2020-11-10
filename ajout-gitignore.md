# Ajout d'un `.gitignore`

Il y a un certain nombre de fichiers que nous ne souhaitons pas *commiter* car ils n'ont pas besoin d'être partagés et peuvent générer des conflits le cas échéant.

Il s'agit généralement des fichiers de cache ou de la base de données SQLite:
- `.DS_Store`
- `*.pyc`
- `db.sqlite3`

Ces fichiers peuvent être ignorés par défaut en ajoutant un fichier `.gitignore`.

## Cas 1 : vous n'avez pas commité ces fichiers.

Ajoutez un fichier `.gitignore` avec le contenu ci-dessous et commitez-le.

```bash
.DS_Store
__pycache__
*.pyc
db.sqlite3
```

## Cas 2 : vous avez déjà commité ces fichiers.

Etapes :
1. Supprimez **tous ces fichiers**.
2. Commitez les changements.
3. Partagez ces changements avec vos co-équipiers (`git pull`, `git push`, etc).
4. Faite ce qui est décrit dans la section **`Cas 1`**.

## Cas 3 : vous avez déjà commité ces fichiers avec un fichier `.gitignore`.

Etapes :
1. Supprimez le **`.gitignore`**.
2. Commitez les changements.
3. Partagez ces changements avec vos co-équipiers (`git pull`, `git push`, etc).
4. Faite ce qui est décrit dans la section **`Cas 2`**.