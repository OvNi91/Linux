# Commandes utiles Linux #

## Pour savoir si un paquet est bien installé #
- dpkg -l | grep nomDuPaquet
	- ii -> Installé
- dpkg --list 'nomDUPaquet'
	- ii >> Installé

## Pour se déplacer dans les dossiers #
- cd (avancer)
- cd .. (reculer)

## Ouvrir un fichier #
- cat nomDuFichier -> Lecture
- nano nomDuFichier -> Ecriture

## Vérifier l'intégrité grâce au SHA256 ##
-  Get-FileHash -Algorithm SHA256 -Path [nomDuFichier]

## Supprimer le disque de la VM #
- nano /etc/apt/sources.list (-> mettre un #devant le disque puis enregistrer)

## Commande help sur un fichier ##
- man [nomDuFichier]

## Passer en mode root #
- su -> entrer (puis rentrer le mdp)

## Voir les update pour apt #
- apt-get update
	- upgrade si on veut appliquer les update dispo

## Afficher les informations du paquet apt #
- apt show apt 

## Lister les fichiers appartenant au paquet apt #
- dpkg -L apt

## Trouver le paquet Debian d'où provient /etc/services #
- dpkg -S /etc/services

## Pour Installer #
- apt install NomDuProgramme

## Mettre en place le ssh ##
1. Vérifier le ssh
	- apt search ssh
2. Installer le ssh
	- apt install ssh
3. Installer le serveur
	- apt install openssh-server

## Ajouter un user #
- [Lien utile pour la création de goupes utilisateur](https://linux.goffinet.org/administration/securite-locale/operations-sur-les-utilisateurs-et-les-groupes/)
- useradd [options] identifiant 
- /usr/sbin/useradd nomDuUser
- Pour utiliser la commande 'adduser' se mettre en mode root avec "su -" et pas seulement 'su'
- Changer ses temps de mdp
	- chage -m [chiffre] [nomUser] --> Set le minimum de temps avant qu'il puisse rechanger son mdp
	- chage -M [chiffre] [nomUser] --> Set le maximum de temps avant que le user puisse changer son mdp

## Voir les dépendances ##
- apt -cache depends zsh

## Les droits Exo TP1 ##
- 0027 -> Dylan l'a dit mdr
- par défaut, c'est 022

## Voir les processus apache en cours ##
- [sudo] systemctl status apache2
	- (578 processus lancés dans le TP)

## Lancer Apache2 ##
- Taper l'adresse IP de la VM dans un moteur de recherche (firefox)
- [Lien utile pour bases de données installation sous linux](https://guillaume-cortes.fr/serveur-web-apache-debian-9/)

## Voir tous les processus ##
- top (équivalent du gestionnaire de tâches)

# Configurer carte réseau (partie 5 TP mini projet) #
## DHCP config ##
- [Lien pour voir une manière de configurer du DHCP](https://wiki.debian.org/fr/DHCP_Client)

## Fichier de configuration réseau ##
- /etc/network/interfaces
- Mieux pour la config DHCP >> cat /etc/dhcp/dhclient.conf

## Afficher tables de routage ##
- ip route 

## DNS et Hosts ##
- [Lien utile pour avoir plus d'informations sur la localisation des fichiers importants](http://www.linux-france.org/~mdecore/linux/doc/memo2/node37.html)
- [Doc Ubuntu sur fichier host](https://doc.ubuntu-fr.org/hosts)

## Résolution DNS / NSS ##
- [Lien expliquant un peu plus l'emplacement des fichiers concernant le DNS local](http://l.github.io/debian-handbook/html/fr-FR/sect.hostname-name-service.html#:~:text=Le%20m%C3%A9canisme%20de%20r%C3%A9solution%20de,noms%20d'h%C3%B4tes%20est%20hosts%20.)

## Paramètres réseau ## 
- [Lien debian avec de plus grandes explications sur les fichiers réseaux dans linux](https://wiki.debian.org/NetworkConfiguration)

## Voir l'état des connexions réseau ##
- nmcli
# Commandes utiles Linux #

## Pour savoir si un paquet est bien installé #
- dpkg -l | grep nomDuPaquet
	- ii -> Installé
- dpkg --list 'nomDUPaquet'
	- ii >> Installé

## Pour se déplacer dans les dossiers #
- cd (avancer)
- cd .. (reculer)

## Ouvrir un fichier #
- cat nomDuFichier -> Lecture
- nano nomDuFichier -> Ecriture

## Vérifier l'intégrité grâce au SHA256 ##
-  Get-FileHash -Algorithm SHA256 -Path [nomDuFichier]

## Supprimer le disque de la VM #
- nano /etc/apt/sources.list (-> mettre un #devant le disque puis enregistrer)

## Commande help sur un fichier ##
- man [nomDuFichier]

## Passer en mode root #
- su -> entrer (puis rentrer le mdp)

## Voir les update pour apt #
- apt-get update
	- upgrade si on veut appliquer les update dispo

## Afficher les informations du paquet apt #
- apt show apt 

## Lister les fichiers appartenant au paquet apt #
- dpkg -L apt

## Trouver le paquet Debian d'où provient /etc/services #
- dpkg -S /etc/services

## Pour Installer #
- apt install NomDuProgramme

## Mettre en place le ssh ##
1. Vérifier le ssh
	- apt search ssh
2. Installer le ssh
	- apt install ssh
3. Installer le serveur
	- apt install openssh-server

## Ajouter un user #
- [Lien utile pour la création de goupes utilisateur](https://linux.goffinet.org/administration/securite-locale/operations-sur-les-utilisateurs-et-les-groupes/)
- useradd [options] identifiant 
- /usr/sbin/useradd nomDuUser
- Pour utiliser la commande 'adduser' se mettre en mode root avec "su -" et pas seulement 'su'
- Changer ses temps de mdp
	- chage -m [chiffre] [nomUser] --> Set le minimum de temps avant qu'il puisse rechanger son mdp
	- chage -M [chiffre] [nomUser] --> Set le maximum de temps avant que le user puisse changer son mdp

## Voir les dépendances ##
- apt -cache depends zsh

## Les droits Exo TP1 ##
- 0027 -> Dylan l'a dit mdr
- par défaut, c'est 022

## Voir les processus apache en cours ##
- [sudo] systemctl status apache2
	- (578 processus lancés dans le TP)

## Lancer Apache2 ##
- Taper l'adresse IP de la VM dans un moteur de recherche (firefox)
- [Lien utile pour bases de données installation sous linux](https://guillaume-cortes.fr/serveur-web-apache-debian-9/)

## Voir tous les processus ##
- top (équivalent du gestionnaire de tâches)

# Configurer carte réseau (partie 5 TP mini projet) #
## DHCP config ##
- [Lien pour voir une manière de configurer du DHCP](https://wiki.debian.org/fr/DHCP_Client)

## Fichier de configuration réseau ##
- /etc/network/interfaces
- Mieux pour la config DHCP >> cat /etc/dhcp/dhclient.conf

## Afficher tables de routage ##
- ip route 

## DNS et Hosts ##
- [Lien utile pour avoir plus d'informations sur la localisation des fichiers importants](http://www.linux-france.org/~mdecore/linux/doc/memo2/node37.html)
- [Doc Ubuntu sur fichier host](https://doc.ubuntu-fr.org/hosts)

## Résolution DNS / NSS ##
- [Lien expliquant un peu plus l'emplacement des fichiers concernant le DNS local](http://l.github.io/debian-handbook/html/fr-FR/sect.hostname-name-service.html#:~:text=Le%20m%C3%A9canisme%20de%20r%C3%A9solution%20de,noms%20d'h%C3%B4tes%20est%20hosts%20.)

## Paramètres réseau ## 
- [Lien debian avec de plus grandes explications sur les fichiers réseaux dans linux](https://wiki.debian.org/NetworkConfiguration)

## Voir l'état des connexions réseau ##
- nmcli
