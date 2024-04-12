# Active_directory-
Nous allons créer un annuaire basé sur un système d'autorisations sélectif en fonction des métiers, des types de comptes et des différentes opétaions . Nous utilserons :
- Windows Server 2022
- Active Directory
- Un serveur DHCP
- Un serveur DNS

## Qu'est ce que Active Directory 

Active Directory est un service d'annuaire, c'est une structure hiérarchique qui stockant des informations sur les objets réseau. AD propose des méthodes pour stocker des données d'annuaire et rendre ces données disponibles aux utilisateurs et administrateur réseau. Celui-ci stocke des informations sur les comptes d'utilisateurs, comme les noms, les mots de passe, les numéros de téléphone et permet aux utilisateurs autorisés du même réseau d'accéder à ces informations.

## Installation de Windows Server et Configuration du Réseaux

Après installation de notre VM on configure le mot de passe de Windows Server : 
![Windowsservermdp](https://github.com/alexander-doumec/active_directory-/assets/147488564/1d3dbf6a-1d31-4702-9708-23cfc962faff)

Voici ce qu'il ce passe ensuite : 
![windowsserver](https://github.com/alexander-doumec/active_directory-/assets/147488564/d342f89c-74fd-4535-bb7c-c5a9fe558542)

On va ensuite s'assurer  que l'adresse IP de notre ordinateur on crée un nouveau réseau sur notre VM avec le DHCP désactiver  
IP chosie : 192.168.100.0/24

![network](https://github.com/alexander-doumec/active_directory-/assets/147488564/0467f93d-6d9e-4e05-b285-6f246d42dd6b)

On accéde à notre panneau de configuration : 

![panneauconfig](https://github.com/alexander-doumec/active_directory-/assets/147488564/29530b02-e72d-435a-8e23-89a5f646afdb)

On accéde ensuite a Centre Réseau : 

![centreréseau](https://github.com/alexander-doumec/active_directory-/assets/147488564/7fe8878e-27b2-4abd-9dea-969ded27b436)

Après avoir accéder à celui on configure l'IPV4 de notre réseau : 

![configip](https://github.com/alexander-doumec/active_directory-/assets/147488564/391ae96f-6308-4d99-816a-87c9b0340220)

Mes configurations : 

![configip(1)](https://github.com/alexander-doumec/active_directory-/assets/147488564/acfb2e03-d58a-40cf-99b7-30ef651eba78)

On verifie que le réseau est bien configurer : 

![ipstatic](https://github.com/alexander-doumec/active_directory-/assets/147488564/80c33052-3de7-4510-86a5-efff98de6f2b)


## Installation de l'outils Active DIrectory 

Une fois Active Directory installer il faut adresser notre serveur principal comme serveur de déploimement , création du nom de domaine dans une nouvelle forêt : 

![AD](https://github.com/alexander-doumec/active_directory-/assets/147488564/57a36207-cf6a-4460-900a-6a40ce2e918b)

Configuration du nouveau mot de passe  spécifications du contrôleur de domaine en DNS :

![AD(2)](https://github.com/alexander-doumec/active_directory-/assets/147488564/66d4cafc-e98a-42b9-9c72-be7bde4623ba)

Le NETBIOS : 
![AD(3)](https://github.com/alexander-doumec/active_directory-/assets/147488564/53030f3d-99b3-4759-af8e-64872dfbbca4)

Une fois ces étapes terminé voici ce qu'affiche notre tableau de bord : 

![AD(4)](https://github.com/alexander-doumec/active_directory-/assets/147488564/a825850f-4db3-4c79-a3db-3a7f3c2fed3a)

