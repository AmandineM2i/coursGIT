# Cours GIT

<b>Cloner un projet</b>
>git clone <nom du projet>

<b>initialiser un projet</b>
>git init

<b>checker les modificartions apportées au projet</b>
>git status

<b>suivre un fichier</b>
>git add <nom du fichier>, <fichier 2>

<b>suivre tout les fichiers</b>
>git add .

<b>sauvegarder en local</b>
>git commit -m "<message>"

<b>envoyer ma version au repo distant</b>
>git push origin main

<br/>
<b>Empêcher la sauvegarde de certains fichiers</b>

<br/>A la racine de votre projet, créez un fichier <i>.gitignore</i> qui contiendra le chemin des fichiers à ignorer

<br/><b>En cas de conflit sur un même fichier</b>

vous avez dans votre fichier un exemple de ceci :

<<<<<<< HEAD
quentin = "blabla"
=======
quentin = "Je suis passé par là"
cyriak = "j'ai modifié ton fichier"
>>>>>>> 1fc9ae27935fae126e63d8b8fbb04e3eaa9b3d72

HEAD : Ce qui est sur votre machine

===== >>>> : Ce qui provient du repo distant

En cas de conflit, vous avez 3 choix possibles : 
- conserver ce qui est sur votre machine 
- conserver ce qui provient du repos distant 
- conserver les deux

Une fois le choix fait, enregistrez les changements et push le tout


### <b>Travailler par branches</b>
Les étapes du cycle de développement : 
- 1. phase de dev 
- créer une branche :
> git checkout -b <nom de la branche> 
- se rendre dessus 
> git switch <nom de la branche> 
- 2. phase de développement 
- Commits et push réguliers sur le repo distant 
- 3. phase de fusion 
- se rendre sur la branche parente 
> git switch <nom de la branche> 
- pull la dernière version du repos distant 
- se rendre sur la branche :
> git switch <ma_branche> 
- merge avec la branche parente :
> git merge <nom de la branche parente> 
- add + commit git add + git commit -m "<message>" 
- push : git push origin <nom de ma branche> 
- j'effectue une pull request 
- validation de la pull request 
- suppression de la branche ( si plus besoin d'elle) 
- on recommence le cycle

- on teste autre chose