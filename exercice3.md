## Exercice 3 - Quiz 

Répond aux questions suivantes:

1. Donne une ligne de commande bash qui permet de lister la liste des utilisateurs d'un système Linux

*cat /etc/passwd*

2. Quelle commande bash permet de changer les droits du fichier **myfile** en rwxr—r-- ?

On peut faire un chmod 744 myfile 
7 pour l'écriture, exécution et la lecture pour le propriétaire du fichier.
4 pour la lecture seule pour le groupe propriétaire du fichier.
4 pour la lecture seule  pour les autres utilisateurs.

3. Comment faire pour que les fichiers **pdf** d'un dépôt local git ne soient pas pris en compte lors d'un **git push** ?

Avec le fichier .gitignore ( à crée dans la racine du dépot si il n'existe pas )
Ouvrir le fichier avec un éditeur de texte 
Et en insérant " \*.pdf "  ( il va ignorer les fichiers pdf )



4. Quelles commandes git utiliser pour fusionner les branches **main** et **test_valide** ?

Il faut basculer dans un premier sur la branche main car la fusion se fera sur celle-ci.
	Pour s'assurer d'être sur la branche main, on peut faire la commande "git checkout main" Ensuite on va faire un "git merge test-valide" pour les fusionner 


5. Donne la(les) ligne(s) de commande(s) bash pour afficher le texte suivant :

```
Malgré le prix élevé de 100$, il a dit "Bonjour !" au vendeur :
- "Bonjour est-ce que ce clavier fonctionne bien ?"
- "Evidemment ! On peut tout écrire avec, que ce soit des pipe | ou bien des backslash \\ !"
- "Même des tildes ~ ?"
- "Evidemment !"
```


Nous pouvons utilisé la commande "echo", suivi d'un guillemet simple avant le début du texte et à la fin de celui-ci. Et pour ne pas que shell interprète les caractères spéciaux mettre des guillemets dans les phrases avec des caractères spéciaux 

echo '
Malgré le prix élevé de 100$, il a dit "Bonjour !" au vendeur :
- "Bonjour est-ce que ce clavier fonctionne bien ?"
- "Evidemment ! On peut tout écrire avec, que ce soit des pipe | ou bien des backslash \\ !"
- "Même des tildes ~ ?"
- "Evidemment !"
'

6. La commande `jobs -l` donne le résultat ci-dessous :

```bash
1wilder@Ubuntu:~$ jobs -l
2[1]  37970 En cours d'exécution   gedit &
3[2]  37971 En cours d'exécution   xeyes &
4[3]- 37972 En cours d'exécution   sleep
```


Quelle commande te permet de mettre en avant le processus **gedit** ?  

La commande fg %1
fg va mettre un processus au premier plan
%1 va choisir le premier de la liste ci dessus en l'occurrence gedit comme indiqué 


7. Quels matériels réseaux sont sur la couche 2 et la couche 3 du modèle OSI ? Donne leurs spécificités.  

Le switch est sur la couche 2 ( liaison des données)
le switch fonctionne en utilisant les adresses MAC pour transférer les données entre les périphériques sur le même réseau local.

Le routeur est sur la couche 3 ( réseau )
le routeur fonctionne à un niveau plus élevé en analysant les adresses IP



8. Quels sont les équivalent PowerShell des commandes bash **cd**, **cp**, **mkdir**, **ls**. 

cd : **Set-Location**
cp : **Copy-Item**
mkdir: **New-Item** ( création ) **Item-Type** ( le type d'item ) **Directory**  ( type fichier )
ls : **Get-ChildItem**

9. Dans la trame ethernet, qu'est-ce que le payload ?  

Le payload est la charge utile, ce sont les données réelles qui sont transportées à travers le réseau. C'est la partie de la trame qui contient les données de l'application ou du protocole qui sont envoyées d'un périphérique à un autre.

10. Pourquoi les classes IP sont remplacées par le CIDR ?

Je ne sais pas
