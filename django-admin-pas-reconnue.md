# Commande `django-admin` non reconnue

## Problème

J'exécute la commande dans mon terminal et j'obtiens l'erreur suivante :

**Mac OS**
```
bash: django-admin: command not found
```

**Windows**
```
'django-admin' n'est pas reconnu en tant que commande interne
ou externe, un programme exécutable ou un fichier de commandes
```

**PowerShell (Windows)**
```
django-admin: Le terme "django-admin" n'est pas reconnu comme nom d'applet de
commande, fonction, fichier de script ou programme exécutable. Vérifiez
l'orthographe du nom, ou si un chemin d'accès existe, vérifiez que le
chemin d'accès est correct et réessayez.
```

## Causes

## Cause 1

Vous n'avez pas installé la librairie `django`.

```bash
pip install django
```

## Cause 2

Vous êtes sur Mac OS ou Linux et vous utilisez `python3`. Vous devez installer dans ce cas vos dépendances avec `pip3`.

```bash
pip3 install django
```

## Cause 3

Vous avez un problème de `PATH`. Voir [ici](./regler-les-problemes-de-path.md).