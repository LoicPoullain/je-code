# Erreur de syntaxe invalide

Si vous obtenez une erreur de syntaxe lorsque vous exécutez une commande du type `pip install django` ou `python manage.py runserver`, c'est que vous êtes dans une console python (qui ne lit que du python).

```
Python 2.7.15 (default, Oct  2 2018, 11:47:18) 
[GCC 4.2.1 Compatible Apple LLVM 10.0.0 (clang-1000.11.45.2)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> pip install django
  File "<stdin>", line 1
    pip install django
              ^
SyntaxError: invalid syntax
>>> 
```

Pour en sortir, tapez `exit()` puis appuyez sur `Entrée`.