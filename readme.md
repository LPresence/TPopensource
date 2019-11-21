Hola

Mise en place d'une infrastructure virtualisée, redondée et sauvegardée.
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
  - 2 CPU
  - 1 NIC
  - 4 HDD

Afin de faciliter et d'optimiser le déploiement de l'infrastructure, la configuration de l'ensemble des services sera effectuée via Ansible.
