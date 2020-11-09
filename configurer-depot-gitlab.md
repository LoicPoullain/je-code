# Configurer un dépôt Gitlab à plusieurs

Ce document explique comment configurer un dépôt Gitlab à plusieurs.

Votre groupe est composé de plusieurs personnes : A et B1, B2, B3, etc.

### Consignes pour la personne A

Allez sur Gitlab et créez un dépôt si ce n'est pas déjà fait. Le depôt est la "boîte" qui va contenir le code de votre projet. Voici comment faire :

![./assets/gitlab1.jpg](./assets/gitlab-1.jpg)
![./assets/gitlab2.jpg](./assets/gitlab-2.jpg)

Vous allez maintenant ajouter votre binôme et votre enseignant comme collaborateur de votre dépôt. Pour cela, allez sur votre depôt GitLab et choisissez le menu Settings | Members dans la fenêtre de gauche. Ajouter votre binôme et votre enseignant comme collaborateur. Vos collègues seront *Maintainer* et votre enseignant sera Reporter.

### Consignes pour toutes les personnes

Chacun de votre côté va maintenant devoir copier ce dépôt sur votre ordinateur. Ouvrez pour cela un terminal.

Vérifiez que git est bien installé en tapant :

```bash
git --version
```

Le numéro de version de git devrait apparaître. Si vous obtenez `Command not found`, merci de vous reporter à cette [page](./regler-les-problemes-de-path.md).

Une fois fait, placez-vous dans le dossier (aussi appelé répertoire) où vous voulez créer votre projet (il peut s'agir du bureau, de mes documents, etc).

> Pour se placer à la racine d'un dossier, il faut utiliser la commande `cd` (normalement vue en SIP).
>
> `cd my_dir` <=> aller dans le sous-dossier `my_dir`
>
> `cd ..` <=> aller dans le dossier  parent

Allez sur Gitlab récupérer l'adresse web de votre dépôt.

![./assets/gitlab3.jpg](./assets/gitlab-3.jpg)

Et maintenant clonez le dépôt dans votre machine (ne le faites pas dans un dossier où il y a déjà des fichiers...)

> git clone l_adresse_de_votre_depot

Un nouveau dossier devrait apparaître avec votre code inclus dedans.

> Si vous obtenez l'erreur `Couldn't find ref remote master`, allez sur le Gitlab (dans le navigateur web) et créez un fichier random (par exemple README.md).

> Si vous obtenez une erreur de certificat (qui sert à crypter vos échanges entre votre ordinateur et Gitlab), vous avez **deux solutions possibles** :
>
> **Solution 1: désactiver SSL (non recommandé)**
>
> A la place d'utiliser la commande `git clone`, utilisez ces commandes :
>
> ```sh
> mkdir saclaylocal # attention, aucun dossier "saclaylocal" ne doit déjà exister
> cd saclaylocal
> git init
> git remote add origin ladresse_du_depot_qui_commence_par_https
> git config http.sslVerify false
> git pull origin master # cela peut prendre un peu de temps
> ```
>
> **Solutin 2: créer une paire de clés SSH (une privée et une publique)**
>
> ![./assets/ssh-key.jpg](./assets/ssh-key.jpg)
>
> Une fois que vous aurez cliqué sur `generate one`, suivez le tutoriel pour en créer une. Lorsque vous générez la clé, laissez tous les champs vides. Pressez juste "Entrée" à chaque fois.
>
> Vous pouvez ensuite afficher votre clé publique via (attention sur Windows, utilisez le Git bash ou le PowerShell):
> ```sh
> cat ~/.ssh/id_rsa.pub
> ```
> Copiez-la ensuite dans le grand rectangle.

Vous pouvez maintenant faire vos commits et "pusher" vos versions sur Gitlab.

```sh
# Voici quelques rappels des commandes git les plus courantes
git status # afficher les fichiers qui sont sélectionnés pour être commités et ceux qui ne le sont pas.
git diff # afficher les modifications depuis le dernier commit
git add my_file_name # ajouter un fichier dans la zone de transit
git commit -m "A message that describes the commit" # créer un commit à partir des fichiers dans la zone de transit.
# Il s'agit d'une sauvegarde (d'une version) de votre code. Partager votre code revient à transmettre des commits.
git push origin master # envoyer vos commits sur le serveur
git pull origin master # récupérer les commits du serveur
```