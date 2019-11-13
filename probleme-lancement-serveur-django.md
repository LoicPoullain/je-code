# Problème de lancement du serveur Django

**Cas 1**

Vérifiez que vous utilisez bien cette commande :

```
python manage.py runserver
```

**Cas 2**

Vérifiez que vous êtes bien dans le dossier où se situe le fichier `manage.py` (et pas dans le dossier parent).

Vous pouvez vous aider de la commande `pwd` pour savoir dans quel dossier vous vous situez.

**Cas 3**

Si vous obtenez l'erreur suivante, c'est que vous utilisez une version 2 de python et non la version 3.

```
 File "manage.py", line 14
   ) from exc
        ^
SyntaxError: invalid syntax
```

Essayez alors avec la commande `python3 manage.py runserver`. Si une autre erreur vous indique qu'il ne trouve pas django, utilisez `pip3 install django`.

**Cas 4**

Vous obtenez l'erreur suivante:

```
UnicodeDecodeError: 'utf-8' codec can't decode byte 0xe9 in position 5: invalid continuation byte
```

Vérifiez que votre nom d'ordinateur ne comporte pas d'accent. S'il y en a un, changez-le.
