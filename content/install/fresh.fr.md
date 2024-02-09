---
title: Installation rapide 
weight : 21
---
{{% notice style="note" title="Attention" icon="exclamation-triangle" %}}
Ne pas utiliser sur une installation existante, à moins de bien vérifier ce que fait le script
(en particulier au niveau de nginx)
{{% /notice %}}

Cette méthode installe tous les composants nécéssaires pour utiliser OST.
elle est simple à utiliser, fonctionne sur un Raspberry Pi, une VM (Virtualbox), ou un pc classique.
Depuis une install Ubuntu vierge, en ligne de commande :

```shell
cd
wget https://raw.githubusercontent.com/gehelem/OST/main/install.sh
chmod +x install.sh
./install.sh
```

Ce script installe tout ce qu'il faut pour avoir un ensemble opérationnel :
- Le serveur Indi
- Nginx
- Quelques index Astrometry.net
- L'interface web OST
- Indiwebmanager
- Un service ostserver

A l'issue de ce script vous pouvez aller créer votre profil indiwebmanager, 
et y démarrer le serveur indi :

![Indiweb](/images/indiweb.png)

Puis aller sur la page d'acceuil OST :

![OST1](/images/ost1.png)