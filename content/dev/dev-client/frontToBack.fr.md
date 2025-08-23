---
title: Messages depuis le client vers le serveur
weight : 30
---
Les messages sont tous composés d'une commande "evt" (commençant par un "F" majuscule... pour "Front") .

## Freadall
Le client demande au serveur de lui renvoyer l'intégralité du contenu des modules.  
{{< highlight json "linenos=inline, hl_lines=3 6-8, style=emacs" >}}
{
    "evt":"Freadall"
}
{{< /highlight >}}
Les messages suivants sont composés d'une clé "mod" précisant l'identifiant du module concerné,  
et d'une cle "dta" contant le détail des informations.

## Fsetproperty
Le client demande au serveur de mettre à jour les éléments d'une propriété d'un module donné.  
{{< highlight json "linenos=inline, hl_lines=3 6-8, style=emacs" >}}
{
    "evt":"Fsetproperty",
    "mod":"Dummy",
    "dta":{
        "extextRW":{
            "elements":{
                "extext1":"torototo",   // valeurs à mettre à jour
                "extext2":"bbbb",       // "
                "extext3":"cccc",       // "
                "extext4":"i1"          // "
            }
        }
    }
}
{{< /highlight >}}
## Flup
Déplacer vers le haut une ligne de la grille.  
{{< highlight json "linenos=inline, hl_lines=3 6-8, style=emacs" >}}
{   
    "evt":"Flup",
    "mod":"Dummy",
    "dta":{
        "agrid":{
            "line":1 // on demande à remonter la seconde ligne
        }
    }
}
{{< /highlight >}}

## Fldown
Déplacer vers le bas une ligne de la grille. 
{{< highlight json "linenos=inline, hl_lines=3 6-8, style=emacs" >}}
{   
    "evt":"Fldown",
    "mod":"Dummy",
    "dta":{
        "agrid":{
            "line":0  // on demande à descendre la première ligne
        }
    }
}
{{< /highlight >}}

## Fldelete
Supprimer une ligne de la grille.  
{{< highlight json "linenos=inline, hl_lines=3 6-8, style=emacs" >}}
{   
    "evt":"Fldelete",
    "mod":"Dummy",
    "dta":{
        "agrid":{
            "line":0  // on demande à supprimer la première ligne
        }
    }
}
{{< /highlight >}}

## Flcreate
Ajouter une ligne à la grille.  
{{< highlight json "linenos=inline, hl_lines=3 6-8, style=emacs" >}}
{   
    "evt":"Flcreate",
    "mod":"Dummy",
    "dta":{
        "agrid":{
            "elements":{
                "int":1,            // valeurs à créer
                "intlov":1,         // "
                "float":2.3,        // "
                "string":"qsdqsdf", // "
                "strlov":"02"       // "
            }
        }
    }
}
{{< /highlight >}}

## Flupdate
Mettre à jour une ligne de la grille.  
{{< highlight json "linenos=inline, hl_lines=3 6-8, style=emacs" >}}
{  
    "evt":"Flupdate",
    "mod":"Dummy",
    "dta":{
        "agrid":{
            "elements":{
                "float":2.3,            // valeurs à modifier
                "int":1,                // "
                "intlov":1,             // "
                "string":"qsdqsdfddddd",// "
                "strlov":"02"           // "    
            },
        "line":1                        // ligne à modifier
        }
    }
}
{{< /highlight >}}

## Fposticon
Le client soumet une action sur le posticon d'un élément.  
{{< highlight json "linenos=inline, hl_lines=3 6-8, style=emacs" >}}
{   
    "evt":"Fposticon",
    "mod":"mainctl",
    "dta":{
        "load":{
            "elements":{
                "focus":{}      // élément qui soumet l'action
            }
        }
    }
}
{{< /highlight >}}

## Fpreicon
Le client soumet une action sur le preicon d'un élément.  
{{< highlight json "linenos=inline, hl_lines=3 6-8, style=emacs" >}}
{
    "evt":"Fpreicon",
    "mod":"mainctl",
    "dta":{
        "unload":{
            "elements":{
                "xxxxxx":{}
            }
        }
    }
}
{{< /highlight >}}

## Fbadge
Le client modifie le badge d'une propriété.  
{{< highlight json "linenos=inline, hl_lines=3 6-8, style=emacs" >}}
{
    "evt":"Fbadge",
    "mod":"Focus",
    "dta":{
        "loadprofile":{}
    }
}
{{< /highlight >}}