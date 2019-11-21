# Mise en place d'une infrastructure virtualisée, redondée et sauvegardée.

## Résumé

Les serveurs seront hébergées sur la plateforme Microsoft Azure.

A l'aide de l'offre étudiante Ynov, nous bénéficions d'un crédit de 100$ pour utiliser cette plateforme.

L'infrastrucure comprend plusieurs serveurs : 

- 3 serveurs avec les services suivants :
  - OpenLDAP
  - FTP
  - Zabbix (monitoring de l'infrastructure)
  
Le déploiement de ces 3 serveurs sera automatisé via Vagrant, un connecteur pour la plateforme Azure est disponible.

Le modèle de ces serveurs est le Standard_F2sv2, avec comme configuration : 
  - 4 GO de RAM
  - 2 vCPU
  - 1 NIC
  - 4 HDD

Afin de faciliter et d'optimiser le déploiement de l'infrastructure, la configuration de l'ensemble des services sera effectuée via Ansible.

Ansible permettra la configuration automatique des 3 serveurs : 

Configuration du serveur LDAP : 
  - Configuration générale :
    - Domaine
    - Identifiants Administrateur
    - Création des utilisateurs
    
Configuration du serveur FTP : 
  - Configuration générale :
    - Partages
    - Utilisateurs
    - Droits d'accès
    
Configuration du serveur Zabbix : 
  - Configuration générale :
    - Création des hôtes à surveiller
    - Création des alertes/notifications
    - Création des utilisateurs
    
## Nommage des serveurs : 

SRV1
  - OpenLDAP
  - FTP
  - Zabbix
    
SRV2
  - OpenLDAP
  - FTP
    
SRV3
  - OpenLDAP
  - FTP

## Configuration réseau

Le plan d'adressage sera :

10.0.0.0/24 

Les serveurs seront configuré en IP statique.

Gateway : 10.0.0.254
SRV1 : 10.0.0.1
SRV2 : 10.0.0.2
SRV3 : 10.0.0.3

Tous les serveurs seront dans le même VLAN
    
