---
title: Messages depuis le client vers le serveur
weight : 30
---

## Fsetproperty
Mise à jour des éléments d'une propriété.  
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

