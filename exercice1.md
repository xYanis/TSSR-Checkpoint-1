## Exercice 1 - Gestion du stockage

Je viens regarder les informations sur mes disques avec la commande **fdisk -l** 
Avec cette commande je constate que deux disques sont bien présent. 
1 disque dur de 10 GB (sdb)
1 disque dur de 25 GB (sda)
Nous allons travailler uniquement sur le deuxième

![2024-03-29 09_15_06-Checkpoint1-SRVDEBIAN  En fonction  - Oracle VM VirtualBox](https://github.com/xYanis/TSSR-Checkpoint-1/assets/161461625/9a32ab8d-9cd4-4c2f-9a4e-f3a0198bb291)


Avec la commande cfdisk /dev/sdb
Nous allons créer les deux partitions attendu
Je séléctionne Dos comme étiquette 

![2024-03-31 14_59_30-Paramètres](https://github.com/xYanis/TSSR-Checkpoint-1/assets/161461625/b107bb93-e90d-45aa-9f1b-a89b6b614859)


Je vais créer ma  première partition 

En séléctionnant "Nouvelle" j'arrive sur l'interface de création. 

![2024-03-31 15_04_32-Checkpoint1-SRVDEBIAN  En fonction  - Oracle VM VirtualBox](https://github.com/xYanis/TSSR-Checkpoint-1/assets/161461625/d3c1296b-b802-46ae-a28b-93521c7a2782)

Je choisis la taille de 6GB et séléctionne "primaire"

![2024-03-31 15_07_36-Checkpoint1-SRVDEBIAN  En fonction  - Oracle VM VirtualBox](https://github.com/xYanis/TSSR-Checkpoint-1/assets/161461625/18ef7e7d-a1c2-4821-b2e8-6204011f638e)

Je viens répéter l'opération pour la deuxième partition avec le reste de la mémoire restante 

![2024-03-31 15_10_43-Checkpoint1-SRVDEBIAN  En fonction  - Oracle VM VirtualBox](https://github.com/xYanis/TSSR-Checkpoint-1/assets/161461625/437758cf-423a-43c9-a52a-a4b2fe28645d)

On constate que les partitions sdb1 et sdb2 ont bien été créées.
Je viens valider mon opération en séléctionnant "Ecrire" et valider avec oui à la question.
Je peux ensuite selectionner "Quitter"

![2024-03-31 15_10_43-Checkpoint1-SRVDEBIAN  En fonction  - Oracle VM VirtualBox](https://github.com/xYanis/TSSR-Checkpoint-1/assets/161461625/2d7a4423-9e47-4e85-86aa-06ba19ab2313)


Nous allons formater en premier le sdb1 avec la commande ci dessous DATA 

sudo mkfs.ext4 -L DATA /dev/sdb1

![2024-03-31 15_21_12-Checkpoint1-SRVDEBIAN  En fonction  - Oracle VM VirtualBox](https://github.com/xYanis/TSSR-Checkpoint-1/assets/161461625/2d23ed0a-d47b-4d33-8b53-c2acb9bf59e8)



Nous allons ensuite formater la partition swap et luji donné le nom SWAP

mkswap -L SWAP /dev/sdb2

![2024-03-31 15_25_33-Checkpoint1-SRVDEBIAN  En fonction  - Oracle VM VirtualBox](https://github.com/xYanis/TSSR-Checkpoint-1/assets/161461625/27441cec-5578-41cc-b3d0-99fb20674dfa)



Nous allons désactiver le swap du sba5 qui est activé et activé le sdb2 ensuite

swapoff /dev/sda 5

swapon /dev/sdb2

![2024-03-31 15_25_56-Checkpoint1-SRVDEBIAN  En fonction  - Oracle VM VirtualBox](https://github.com/xYanis/TSSR-Checkpoint-1/assets/161461625/eba2d365-d256-4b42-a131-2285966441a0)




