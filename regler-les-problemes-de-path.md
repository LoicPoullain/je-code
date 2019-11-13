# Régler les problèmes de `PATH`

## Problème

J'exécute une commande dans mon terminal et j'obtiens l'erreur suivante :

**Mac OS**
```
bash: python: command not found
```

**Windows**
```
'python' n'est pas reconnu en tant que commande interne
ou externe, un programme exécutable ou un fichier de commandes
```

**PowerShell (Windows)**
```
python: Le terme "python" n'est pas reconnu comme nom d'applet de
commande, fonction, fichier de script ou programme exécutable. Vérifiez
l'orthographe du nom, ou si un chemin d'accès existe, vérifiez que le
chemin d'accès est correct et réessayez.
```

Cela peut survenir sur un certain nombre de commandes : `git`, `python`, `django-admin`, `pip`, `psql`, etc.

## Causes

### Cause 1

Vous n'avez tout simplement pas installé le programme (ou la librairie python).

### Cause 2

L'ordinateur ne sait pas où se situe l'exécutable (ou les scripts python). 

Il va falloir lui indiquer en modifiant ce qu'on appelle le `PATH`. Le `PATH` est une liste de répertoires (=dossiers) où votre ordinateur va regarder s'il trouve l'exécutable (ou le script python).

## Solution

Vous devez trouver par vous-même où se situe votre exécutable (petite recherche sur Google et dans vos dossiers). 

Par exemple, pour la commande python, sous Windows, si vous avez installé python depuis [le site officiel](https://www.python.org/downloads/), le nom du dossier hôte s'appelle probablement `C:\Program Files\Python37` (ici la version est 3.7). Sous Mac, le dossier s'appelle probablement `/Library/Frameworks/Python.framework/Versions/3.6/bin` (Pour trouver le numéro de version, exécutez la commande `ls /Library/Frameworks/Python.framework/Versions`).

> Attention pour le chemin du répertoire sur Windows : si le chemin ne fonctionne pas (vous avez toujours le `command not found`), vérifiez que vous avez utilisé le nom `Program Files` et pas `Programmes`.

Une fois le chemin du répertoire récupéré, vous allez donc modifier le `PATH`.

### Mac OS

Sous Mac, il faut le faire via la ligne de commande avec ces instructions :

```
cd
nano .bash_profile
```

Un texte apparaît sur l'écran. Utilisez les flèches pour ajouter cette ligne (de préférence vers le bas):

```
export PATH="le_chemin_du_dossier:${PATH}"
```

Pour fermer, tapez `Ctrl`+`X` puis `Y` puis `Enter`. Ensuite rentrez la commande suivante pour prendre en compte les modifications.

```
source .bash_profile
```

Ouvrez maintenant un nouveau terminal, cela devrait fonctionner.

### Mac OS (version récente)

Si cela ne fonctionne pas, c'est que vous utilisez une version récente de Mac qui utilise `zsh`.

TODO

### Windows


Sur Windows, procédez comme suit :

![variables-environnement-Windows.jpg](./assets/variables-environnement-Windows.jpg)

Une nouvelle fenêtre apparaît où vous pouvez alors rentrer une nouvelle ligne avec le nom du répertoire. Cliquez ensuite sur les boutons ok.

Vous devrez réouvrir votre terminal pour que les modifications soient prises en compte.
