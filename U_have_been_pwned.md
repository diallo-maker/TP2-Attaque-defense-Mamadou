# Travail 2 par *Diallo Mamadou Bobo* *1050*

## Attaque (exploit).

Voici les étapes détaillées pour pouvoir modifier le courriel / téléphone sur la page demandée:

- Test des ports ouverts de l'addresse IP (http://192.168.220.10/) avec Nmap (scan intensif).
- Le port 22(ssh) est ouvert donc on peut s'y connecter  ![nmap](nmap.png)

- Test de la connection par ssh(le id c'est bob).
- Le mot de passe peut être déduis par les anciens mots de passe (3 filles : Jane (5 juin 2001), Patricia (9 novembre 2011) et Sophie (10 décembre 2014)).
![SSH]('SSH_connection'.png)
![Test mot de passe](testmdp.png)

- Une fois connecter, il faut chercher l'emplacement du fichier html du site web.
- Il se trouve dans /var/www/html. La commande cd /var/www/html (cd + l'emplacement pour t'y rendre) et apres (ls -al) pour afficher les fichiers et dossiers.
![emplacement fichier html](emplacement.png)

## 1ère modification: changer le numéro de téléphone.
- On utilise la commande: nano (le nom du fichier) nano contact.html  pour acceder et changer le fichier.
![contact](modification.png)

## 2 ème modification: le lien mailto.

- On est dejà dans le fichier de contact donc on doit juste changer le lien à l'emplacement "Par courriel" par "<a href ="ouch.hacked@cem.ca">
- Une fois le contact changer, on fait : ctrl+X pour sortir et enregistrer le fichier html.
![mailto](mailto.png)


## 3 ème modification: supprimmer les images de réalisation.

- On fait la commande nano realisation.html pour acceder au fichier et supprimer les images demandées.
- À l'eplacement < img src =""> on supprime le contenu entre les "" et les images seront supprimer.
- Une fois changer, on fait : ctrl+X pour sortir et enregistrer le fichier html.
![réalisation](realisation.png) 


## Les résultats des modifications.

- En rechargeant la page, on constate que le numéro de téléphone a été modifié, les images supprimées et le courriel changé.
![contact](resultat_contact.png)
![réalisation](resultat_realisation.png)
![lien](lien_resultat.png)


## Correctif 1
## fermer les ports non utiliser (22.80)

Commandes à effectuer ou étapes à mettre en place. 

Capture d'écran de l'exploit qui ne fonctionne plus.

## Correctif 2 (indépendant du correctif 1)
## avoir des mots de passes plus compliquer.

Commandes à effectuer ou étapes à mettre en place.

Capture d'écran de l'exploit qui ne fonctionne plus. 

## Correctif 3

Commandes à effectuer ou étapes à mettre en place. 

Capture d'écran de l'exploit qui ne fonctionne plus.
