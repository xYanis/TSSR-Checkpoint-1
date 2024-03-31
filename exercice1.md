## Exercice 1 - Gestion du stockage

Je viens regarder les informations sur mes disques avec la commande fdisk -l 
Avec cette commande je constate que deux disques sont bien présent. 
1 disque dur de 10 GB (sdb)
1 disque dur de 25 GB (sda)
Nous allons travailler uniquement sur le deuxième



Avec la commande cfdisk /dev/sdb
Nous allons crée les deux partitions attendu

Pour la première ( sda1) nous allons la monter en 6B
Et pour la deuxième (sda2 ) en 19GB
