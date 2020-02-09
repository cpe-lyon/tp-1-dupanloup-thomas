# Compte Rendu TP1 - DUPANLOUP - THOMAS
## Exercice 2
### Manuel
**1. A l’aide du manuel, identifiez le rôle de la commande which**
>which donne le chemin d’accès  absolu du fichier passé en argument. 

**2. Quand on consulte une page du manuel, comment peut-on rechercher un terme (par exemple, chercher
le terme option dans la page de manuel de which ?** 
>Pour chercher un terme dans une page d’un manuel on utilise la commande : $man which | grep option
Une autre option est de lancer le manuel puis d’utiliser / et de taper le mot cherché. On se déplace ensuite entre les résultats en utilisant la touche n (majuscule pour précédent/minuscule pour suivant).

**3. Comment quitte-t-on le manuel ?**
>Il est possible de quitter le manuel à tout moment en utilisant la touche "q".

**4. Chaque section du manuel a une première page, qui présente le contenu de la section. Afficher la
première page de la section 6 ; de quoi parle cette section ?**<br>
>La section 6 correspond aux jeux. On y accède en utilisant la commande $man 6 intro.<br>

### Navigation dans l’arborescence des fichiers<br>

**1. allez dans le dossier /var/log**<br>
>$cd /var/log

**2. remontez dans le dossier parent (/var) en utilisant un chemin relatif**
>cd ..

**3. retournez dans le dossier personnel**
>cd ~

**4. revenez au dossier précédent (/var) sans utiliser de chemin**
>cd -
>
**5. essayez d’accéder au dossier /root ; que se passe-t-il ?**<br>
>Lorsque l’on essaye d’acceder au dossier root le shell renvoit une erreur car nous n’avons pas l’autorisation root. Pour y acceder il faut entrer la commande $su -
>
**6. essayez la commande sudo cd /root ; que se passe-t-il ? Expliquez**<br>
>Le shell nous indique que la commande n'est pas connue pour sudo
>
**7. à partir de votre dossier personnel, créez l’arborescence suivante :**
>Afin de créer notre arboressence nous utilisons les commandes mkdir ainsi que touch. 
>$sudo mkdir dossier1
>$sudo touch dossier1/fichier1
>$sudo mkdir dossier2/dossier2.1 dossier2/dossier2.2 -p
>$sudo touch dossier2/dossier2.2/fichier1 dossier2/dossier2.2/fichier2

**8. revenez dans votre dossier personnel ; à l’aide de la commande rm, essayez de supprimer Fichier1, puis
Dossier1 ; que se passe-t-il ?**<br>
>La commande rm permet bien de supprimer le fichier1 mais elle ne permet pas de supprimer de dossier; ainsi le dossier1 n’est pas supprimé.

**9. quelle commande permet de supprimer un dossier ?**
>La commande qui permet de supprimer un dossier est $sudo mkdir [dossier]
> 
**10. que se passe-t-il quand on applique cette commande à Dossier2 ?**
>Le shell nous renvoit une erreur puisque le dossier n’est pas vide.

**11. comment supprimer en une seule commande Dossier2 et son contenu ?**
>On utilise la commande $sudo rm -r dossier1

### Commandes importantes <br>

**1. Quelle commande permet d’afficher l’heure ? A quoi sert la commande time ?**
>La commande qui nous permet d’afficher l’heure est la commande $date. La commande $time nous permet de mesurer le temps utilisé par une certaine commande.
>
**2. Dans votre dossier personnel, tapez successivement les commandes ls puis la ; que peut-on en déduire
sur les fichiers commençant par un point ?**
>La commande $ls affiche l’ensemble des fichiers dossiers. La commande $la est un raccourci de la commande $la correspond à la commande $ls -A qui en plus d’afficher l’ensemble des fichiers affiche en plus les fichiers cachés ( ceux commençant par un point )
>
**3. Où se situe le programme ls ?**

> Pour savoir ou est située la commande ls on utilise la commande $which ls. Le shell nous indique que la commande se trouve dans _bin_/ls
> 
**4. Essayez la commande ll. Existe-t-il une entrée de manuel pour cette commande ? Utilisez les commandes alias ou alias pour en savoir plus sur la nature de cette commande.**
>La commande ll ne dispose pas d’entrée dans le manuel. Ce qui est normal puisqu’il s’agit aussi d’un raccouri cette fois ci de la commande $ls -l . Cette commande permet d’afficher plus de détails sur les fichiers et dossiers ce trouvant dans le répertoir courant. De plus la commande alias permet de connaitre les raccourci (par exemple que $la correspond à $ls -a).
>
**5. Quelle commande permet d’afficher les fichiers contenus dans le dossier /bin ?**
>Pour obtenir le contenu de /bin on utilise la commande $ls /bin

**6. Que fait la commande ls .. ?**
>La commande $ls .. permet de faire l’inventaire du dossier parent au dossier courant.
>
**7. Quelle commande donne le chemin complet du dossier courant ?**
>Il s'agit de la commande $pwd.

**8. Que fait la commande echo 'yo' > plop exécutée 2 fois ?**
>La commande echo permet d’imprimer le message ‘yo’. En faisant “> plop” on change la sortie standard ( le terminal ) en un fichier appellé plop. Si on utilise deux fois cette commande rien ne se passe de nouveau.
>
**9. Que fait la commande echo 'yo' >> plop exécutée 2 fois ?**
>Lorsque l’on utilise la commande $echo ‘yo’ >> plop cette commande va écrire dans le fichier plop le message ‘yo’ à la suite de ce qui a été écrit avant.
>
**10. A quoi sert la commande file ? Essayez la sur des fichiers de types différents.**
>La commande file permet de déterminer le type d’un fichier.
>
**11. Créez un fichier toto qui contient la chaîne Hello Toto ! ; créer ensuite un lien titi vers ce fichier**
> 
> Afin de créer un fichier toto qui contient la chaine de caractère “hello toto !” on utilise la commande : $echo “Hello Toto !” > toto
On créer ensuite un lien entre les fichiers avec la commande : $ln toto titi
On va ensuite modifier toto avec la commande $echo “Hello titi !” >> toto
On remarque que cela modifie aussi le fichier titi. Car titi s’agit d’un lien vers le fichier toto ainsi lorsque toto est modifié alors titi est modifié aussi.
Cependant lorsque l’on supprime toto, titi n’est pas supprimmé avec la commande ln toto titi. Modifiez à présent le contenu de toto et affichez le contenu de titi :
qu’observe-t-on ? Supprimez le fichier toto ; quelle conséquence cela a-t-il sur titi ?**

**12. Créez à présent un lien symbolique tutu sur titi avec la commande ln -s titi tutu. Modifiez le
contenu de titi ; quelle conséquence pour tutu ? Et inversement ? Supprimez le fichier titi ; quelle
conséquence cela a-t-il sur tutu ?**
>Lorsque l’on modifie titi ou tutu cela modifie l’autre aussi. Cependant lorsque l’on supprime titi, tutu devient un lien symbolique cassé ( Broken Symbolic Link ). Ce fichier n’est plus utilisable.

**13. Affichez à l’écran le fichier /var/log/syslog. Quels raccourcis clavier permettent d’interrompre et
reprendre le défilement à l’écran ?**
>CTRL + S Pour interrompre le défilement
>CTRL + Q Pour reprendre le défilement

**14. Affichez les 5 premières lignes du fichier /var/log/syslog, puis les 15 dernières, puis seulement les
lignes 10 à 20.**
>La commande $head -5 /_var_/log/syslog permet d’afficher les 5 premières lignes du fichier.
La commande $tail -10 _var/log/syslog_ permet d’afficher les 10 dernières lignes du fichier.

**15. Que fait la commande dmesg | less ?**
>La commande dmesg | less permet d’affichier les messages du kernel. De plus less permet d’affichier le résultat sous forme de page.

**16. Affichez à l’écran le fichier /etc/passwd ; que contient-il ? Quelle commande permet d’afficher la page
de manuel de ce fichier ?**
>Il contient toutes les informations relatives aux utilisateurs.
$man _etc/passwd_ contient le manuel de ce fichier.
>
**17. Affichez seulement la première colonne triée par ordre alphabétique inverse**
>$cat  /etc/passwd  | cut -d ":" -f 1 | sort -rd
>
**18. Quelle commande nous donne le nombre d’utilisateurs ayant un compte sur cette machine (pas seulement les utilisateurs connectés) ?**
>La commande "w" permet de voir le nombre d'utilisateur.

**19. Combien de pages de manuel comportent le mot-clé conversion dans leur description ?**
>man -k conversion |wc -l , ce qui donne 4 pages de manuel.

**20. A l’aide de la commande find, recherchez tous les fichiers se nommant passwd présents sur la machine**
> nd /  -name "passwd" | grep -o passwd | wc -l
> 

**21. Modifiez la commande précédente pour que la liste des fichiers trouvés soit enregistrée dans le fichier
~/list_passwd_files.txt et que les erreurs soient redirigées vers le fichier spécial /dev/null**
>find /  -name "passwd" | grep -o passwd | wc -l  > _/list_passwd_files.txt_
>find /  -name "passwd" | grep -o passwd | wc -l 2>> _/list_passwd_files.txt_
>

**22. Dans votre dossier personnel, utilisez la commande grep pour chercher où est défini l’alias ll vu
précédemment**
>$grep "ll" -r
>d'après le résultat l'alias est est défini dans le fichier .bashrc.

**23. Utilisez la commande locate pour trouver le fichier history.log.**
>$ locate history.log
>/var/log/apt/history.log

**24. Créer un fichier dans votre dossier personnel puis utilisez locate pour le trouver. Apparaît-il ? Pourquoi ?**
>$touch test
>$locate test
> On ne trouve pas le nouveau fichier test avec la commande locate puisque la base n'a pas été mise à jour via la commande updatedb.

## Exercice 4
**Pour obtenir la forme voulue:**
>PS1='\e[35m[\A] - ${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;36m\]\w\[\033[00m\]\$'
