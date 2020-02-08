# Compte Rendu TP1 - DUPANLOUP - THOMAS
## Exercice 2
### Manuel

**1. A l’aide du manuel, identifiez le rôle de la commande which** <br>
which donne le chemin d’accès  absolu du fichier passé en argument. <br>
**2. Quand on consulte une page du manuel, comment peut-on rechercher un terme (par exemple, chercher
le terme option dans la page de manuel de which ?** <br>
**3. Comment quitte-t-on le manuel ?**<br>
**4. Chaque section du manuel a une première page, qui présente le contenu de la section. Afficher la
première page de la section 6 ; de quoi parle cette section ?**<br>
### Navigation dans l’arborescence des fichiers<br>
**1. allez dans le dossier /var/log**<br>
**2. remontez dans le dossier parent (/var) en utilisant un chemin relatif**<br>
**3. retournez dans le dossier personnel**<br>
**4. revenez au dossier précédent (/var) sans utiliser de chemin**<br>
**5. essayez d’accéder au dossier /root ; que se passe-t-il ?**<br>
**6. essayez la commande sudo cd /root ; que se passe-t-il ? Expliquez**<br>
**7. à partir de votre dossier personnel, créez l’arborescence suivante :**<br>
**8. revenez dans votre dossier personnel ; à l’aide de la commande rm, essayez de supprimer Fichier1, puis
Dossier1 ; que se passe-t-il ?**<br>
**9. quelle commande permet de supprimer un dossier ?**<br>
**10. que se passe-t-il quand on applique cette commande à Dossier2 ?**<br>
**11. comment supprimer en une seule commande Dossier2 et son contenu ?**<br>
### Commandes importantes <br>
**1. Quelle commande permet d’afficher l’heure ? A quoi sert la commande time ?**<br>
**2. Dans votre dossier personnel, tapez successivement les commandes ls puis la ; que peut-on en déduire
sur les fichiers commençant par un point ?**<br>
**3. Où se situe le programme ls ?**<br>
**4. Essayez la commande ll. Existe-t-il une entrée de manuel pour cette commande ? Utilisez les commandes alias ou alias pour en savoir plus sur la nature de cette commande.**<br>
**5. Quelle commande permet d’afficher les fichiers contenus dans le dossier /bin ?**<br>
**6. Que fait la commande ls .. ?**<br>
**7. Quelle commande donne le chemin complet du dossier courant ?**<br>
**8. Que fait la commande echo 'yo' > plop exécutée 2 fois ?**<br>
**9. Que fait la commande echo 'yo' >> plop exécutée 2 fois ?**<br>
**10. A quoi sert la commande file ? Essayez la sur des fichiers de types différents.**<br>
**11. Créez un fichier toto qui contient la chaîne Hello Toto ! ; créer ensuite un lien titi vers ce fichier**<br>
avec la commande ln toto titi. Modifiez à présent le contenu de toto et affichez le contenu de titi :
qu’observe-t-on ? Supprimez le fichier toto ; quelle conséquence cela a-t-il sur titi ?**<br>
**12. Créez à présent un lien symbolique tutu sur titi avec la commande ln -s titi tutu. Modifiez le
contenu de titi ; quelle conséquence pour tutu ? Et inversement ? Supprimez le fichier titi ; quelle
conséquence cela a-t-il sur tutu ?**<br>
**13. Affichez à l’écran le fichier /var/log/syslog. Quels raccourcis clavier permettent d’interrompre et
reprendre le défilement à l’écran ?**<br>
**14. Affichez les 5 premières lignes du fichier /var/log/syslog, puis les 15 dernières, puis seulement les
lignes 10 à 20.**<br>
**15. Que fait la commande dmesg | less ?**<br>
**16. Affichez à l’écran le fichier /etc/passwd ; que contient-il ? Quelle commande permet d’afficher la page
de manuel de ce fichier ?**<br>
**17. Affichez seulement la première colonne triée par ordre alphabétique inverse**<br>
**18. Quelle commande nous donne le nombre d’utilisateurs ayant un compte sur cette machine (pas seulement les utilisateurs connectés) ?**<br>
**19. Combien de pages de manuel comportent le mot-clé conversion dans leur description ?**<br>
**20. A l’aide de la commande find, recherchez tous les fichiers se nommant passwd présents sur la machine**<br>
**21. Modifiez la commande précédente pour que la liste des fichiers trouvés soit enregistrée dans le fichier
~/list_passwd_files.txt et que les erreurs soient redirigées vers le fichier spécial /dev/null**<br>
**22. Dans votre dossier personnel, utilisez la commande grep pour chercher où est défini l’alias ll vu
précédemment**<br>
**23. Utilisez la commande locate pour trouver le fichier history.log.**<br>
**24. Créer un fichier dans votre dossier personnel puis utilisez locate pour le trouver. Apparaît-il ? Pourquoi ?**<br>

## Exercice 3
**1. Copiez le fichier /var/log/syslog dans votre dossier personnel sous le nom log.txt, puis ouvrez-le avec
nano**<br>
**2. Remplacez toutes les occurrences du mot kernel par le mot noyau**<br>
**3. Déplacer les 10 premières lignes à la fin du fichier**<br>
**4. Annulez cette action**<br>
**5. Enregistrez le fichier avant de quitter nano**<br>

## Exercice 4
