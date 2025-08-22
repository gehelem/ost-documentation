---
title: Messages depuis le client vers le serveur
weight : 30
---
<<<<<<< HEAD
Les messages sont tous composés d'une commande "evt" (commençant par un "F" majuscule... pour "Front") .

## Freadall
Le client demande au serveur de lui renvoyer l'intégralité du contenu des modules.  
{"evt":"Freadall"}

Les messages suivants sont composés d'une clé "mod" précisant l'identifiant du module concerné,  
et d'une cle "dta" contant le détail des informations.

## Fsetproperty
Le client demande au serveur de mettre à jour les éléments d'une propriété d'un module donné.
=======

## Fsetproperty
Mise à jour des éléments d'une propriété.  
>>>>>>> origin/2-document-json-messages
{"evt":"Fsetproperty","mod":"Dummy","dta":{"extextRW":{"elements":{"extext1":"torototo","extext2":"bbbb","extext3":"cccc","extext4":"i1"}}}}

## Flup
Déplacer vers le haut une ligne de la grille.  
{"evt":"Flup","mod":"Dummy","dta":{"agrid":{"line":0}}}
## Fldown
Déplacer vers le bas une ligne de la grille.  
{"evt":"Fldown","mod":"Dummy","dta":{"agrid":{"line":0}}}

## Fldelete
Supprimer une ligne de la grille.  
{"evt":"Fldelete","mod":"Dummy","dta":{"agrid":{"line":0}}}

## Flcreate
Ajouter une ligne à la grille.  
{"evt":"Flcreate","mod":"Dummy","dta":{"agrid":{"elements":{"int":1,"intlov":1,"float":2.3,"string":"qsdqsdf","strlov":"02"}}}}

## Flupdate
Mettre à jour une ligne de la grille.  
{"evt":"Flupdate","mod":"Dummy","dta":{"agrid":{"elements":{"float":2.3,,"int":1,"intlov":1,,,"string":"qsdqsdfddddd","strlov":"02",},"line":1}}}}

<<<<<<< HEAD
## Fposticon
Le client soumet une action sur le posticon d'un élément.  
{"evt":"Fposticon","mod":"mainctl","dta":{"load":{"elements":{"focus":{}}}}}

## Fpreicon
Le client soumet une action sur le preicon d'un élément.  
{"evt":"Fpreicon","mod":"mainctl","dta":{"unload":{"elements":{"xxxxxx":{}}}}}

## Fbadge
Le client modifie le badge d'une propriété.  
=======
>>>>>>> origin/2-document-json-messages
