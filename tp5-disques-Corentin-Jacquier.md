

# 👨‍💻 TP5 - Gestion des disques 

CPE Lyon - 4ETI, 3IRC & 3ICS - Année 2022/2023 Administration Système

Corentin JACQUIER ICS

## Disques et partitions

D'abord, on ajoute un disque dur de 5 go à notre VM via l'interface vSphère : 

<img src="https://cdn.discordapp.com/attachments/1017478318934724638/1026393078921175062/unknown.png">

On verifie si le disque apparait bien dans la vm, on liste les disques avec la commande `lsblk` : 

<img src="https://cdn.discordapp.com/attachments/1017478318934724638/1026393857165905930/unknown.png">

Le nouveau disque possède le nom '*sdb*'.

On peut voir le détail du disque avec la commande `sudo fdisk -l /dev/sdb` :

<img src="https://cdn.discordapp.com/attachments/1017478318934724638/1026394682248405072/unknown.png">
 
 On ajoute les partitions avec la commande `sudo fdisk /dev/sdb`, on fait d'abord `n` pour new, puis on choisie le premier secteur (1), et le dernier secteur qui est le stockage (+2Go) : 

<img src="https://cdn.discordapp.com/attachments/1017478318934724638/1026400964627935272/unknown.png">

On fait de meme avec une deuxième partition de 3 go. 

