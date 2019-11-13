# Problème d'installation de Django

Pour installer Django globalement, exécutez la commande suivante :

```
pip install django
```

## Erreur 1

Vous obtenez une de ces erreurs:

```
bash: pip: command not found
```

**Windows**
```
'pip' n'est pas reconnu en tant que commande interne
ou externe, un programme exécutable ou un fichier de commandes
```

**PowerShell (Windows)**
```
pip: Le terme "pip" n'est pas reconnu comme nom d'applet de
commande, fonction, fichier de script ou programme exécutable. Vérifiez
l'orthographe du nom, ou si un chemin d'accès existe, vérifiez que le
chemin d'accès est correct et réessayez.
```

:point_right: [Consultez cette page](regler-les-problemes-de-path.md).

## Erreur 2

Si vous obtenez l'erreur suivante, relancez votre terminal en mode administrateur (click droit sur l'icône du terminal > choisir "en tant qu'administrateur").

```
Could not install packages due to an EnvironmentError: [WinError 5] Accès refusé: 'c:\\program files\\python37\\Lib\\site-packages\\pytz'
Consider using the `--user` option or check the permissions.
```
