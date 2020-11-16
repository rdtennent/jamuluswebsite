---
layout: wiki
title: "Gestion d'un serveur"
lang: "fr"
permalink: "/wiki/Running-a-Server"
---

# Gestion d'un serveur

## Ai-je besoin de mon propre serveur pour utiliser Jamulus ?

NON !
{: .doubletextsize .red }


Il suffit juste de choisir un des serveurs (celui de quelqu'un d'autre) dans la liste des serveurs publics, et d'y aller !

**D'accord, mais si je ne veux pas que des inconnus nous dérangent ?** Une fois que vous et vos ami·e·s êtes connecté·e·s à un serveur public, appuyez sur les boutons "_solo_" des musiciens avec lesquels chacun de vous veut jouer. Si vous n'êtes pas en solo, vous verrez une icône "muet" sur votre canal dans la console de mixage Jamulus. Et vous ne les entendrez pas.

## Cela semble trop simple !

OK, si vous voulez vraiment gérer votre propre serveur, il est **très important** que vous lisiez et compreniez quel type de serveur vous voulez faire fonctionner :

<div class="fx-row fx-row-start-xs button-container">
  <a href="Choosing-a-Server-Type" class="button fx-col-100-xs" target="_blank" rel="noopener noreferrer">En savoir plus sur les types de serveurs</a>
</div>

… puis revenez ici lire la suite.

### Vitesse et latence

**_La capacité du serveur lui-même (et du réseau sur lequel il se trouve) n'est PAS le principal facteur déterminant de la qualité d'une session Jamulus !_**

On attribue souvent au serveur des problèmes qui sont en fait des problèmes _coté client_. Cela dépend beaucoup du [matériel des musiciens et musiciennes](Hardware-Setup), des réseaux sur lesquels ils se trouvent, de leur fournisseur d'accès et de leur respect de la [règle numéro un](Getting-Started#vous-avez-des-problèmes-vous-ne-vous-en-sortez-pas). Il n'y a donc aucune garantie que vous obtieniez une latence plus faible ou de meilleures performances globales en ayant votre propre serveur.

Si vous prévoyez de jouer régulièrement avec les mêmes personnes, **il est fortement conseillé** de s'assurer d'abord que chaque membre du groupe est en mesure d'utiliser Jamulus correctement. Pour ce faire, trouvez un serveur public avec un temps de ping raisonnable pour chacun d'entre vous (20ms ou moins peut-être), connectez-vous tous à ce serveur et travaillez à résoudre les problèmes individuels (en vérifiant qu'ils peuvent suivre la [règle numéro un](Getting-Started#vous-avez-des-problèmes-vous-ne-vous-en-sortez-pas) en particulier). Utilisez la technique "_solo_" ci-dessus pour éviter d'être interrompu si nécessaire.

Une fois les problèmes résolus de cette manière, vous pouvez alors envisager d'héberger votre propre serveur soit chez vous, soit sur un hôte dans le _Cloud_ comme Amazon, ce qui pourrait entraîner une meilleure latence qu'un serveur fonctionnant à domicile. Par exemple, voir [ce guide d'utilisation de AWS Lightsail](https://www.facebook.com/notes/jamulus-online-musicianssingers-jamming/howto-idiots-guide-to-installing-jamulus-server-on-amazon-aws-lightsail-ubuntu-i/507719749802976/) par [Simon Tomlinson](https://www.facebook.com/simon.james.tomlinson?eid=ARBQoY3KcZAtS3pGdLJuqvQTeRSOo4gHdQZT7nNzOt1oPMGgZ4_3GERe-rOyH5PxsSHVYYXjWwcqd71a), utilisateur de Jamulus (_Facebook_).

### Et la bande passante ?

Prenons l'exemple d'une session classique avec quatre musiciens ou musiciennes, pour lesquelles il faut 200Kbps * 4 = 800Kbs (0,8Mbps) en débit montant et descendant. Donc, si vous avez une connexion haut débit de 10 Mbits descendant (_Download_) et de 1 Mbits montant (_Upload_), vous risquez de commencer à manquer de bande passante si une cinquième personne se joint à la session. En particulier si des musiciens ou musiciennes choisissent des paramètres qui augmentent leur utilisation de la bande passante. Vous devriez peut-être [vérifier que vous avez une vitesse suffisante](https://fast.com) pour cela. Pour [en savoir plus sur l'utilisation de la bande passante](Network-Requirements) selon différents paramètres de qualité.

### En résumé

- Envisager d'utiliser un serveur _dans le Cloud_ ou un serveur dédié en datacenter si vous avez des problèmes de bandes passante ou un accès internet avec un mauvais temps de réponse (_ping_).

- Le serveur "physique" devrait avoir un processeur avec une fréquence CPU d'au moins 1,6 GHz et au minimum 1 Go de RAM

- Il est possible que vous deviez ajuster les règles de filtrages du pare-feu (_firewall_) fonctionnant sur votre machine, votre routeur, ou la machine distante.

- Gérer un **serveur privé** (_mais pas pour un serveur public_) à domicile nécéssite de [rediriger le port](Running-a-Private-Server) utilisé par Jamulus sur votre routeur ou _box internet_.

- Jamulus ne supporte pas IPv6 pour le moment


## Tout est clair ? Alors, c'est parti !

### [Pour les utilisateur·trice·s de Windows ou MacOS](Server-Win-Mac)
### [Pour les utilisateur·trice·s de Linux](Server-Linux)
### [Pour les utilisateur·trice·s de Raspberry Pi](Server-Rpi)

Les gestionnaires de serveurs pourraient également être intéressé·e·s par le téléchargement de [cet ensemble d'outils utiles](https://github.com/corrados/jamulus/tree/master/tools) à partir du dépôt Jamulus (cloner le "_repo_" Git avec la commande `git submodule update --init`).

## Vous avez des problèmes ? Des Questions ?

Jetez un œil à la section [Dépannage du serveur](Server-Troubleshooting)