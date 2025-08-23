---
title: Messages en provenance du serveur
weight : 30
---


## moduledump
Un message par module, contenant toutes ses propriétés.  
[exemple](/example.json)

## ap
Mise à jour de toutes les informations d'une propriété donnée.
{{< highlight json "linenos=inline, hl_lines=3 6-8, style=emacs" >}}
{
    "evt": "ap",
    "modules": {
        "Focus": {
            "properties": {
                "saveprofile": {
                    "badge": false,
                    "elements": {
                        "name": {
                            "autoupdate": true,
                            "badge": false,
                            "directedit": true,
                            "hint": "",
                            "label": "",
                            "order": "00",
                            "posticon": "save",
                            "type": "string",
                            "value": "testpour REné"
                        }
                    },
                    "enabled": true,
                    "freevalue": "",
                    "gridheaders": [
                        "name"
                    ],
                    "hasGraph": false,
                    "hasGrid": false,
                    "hasprofile": false,
                    "label": "Sauvegarder le profil",
                    "level1": "Module",
                    "level2": "Profils",
                    "order": "01",
                    "permission": 2,
                    "posticon1": "",
                    "posticon2": "",
                    "preicon1": "",
                    "preicon2": "",
                    "rule": 0,
                    "showElts": true,
                    "status": 2
                }
            }
        }
    }
}
{{< /highlight >}}
## se
Mise à jour des valeurs des éléments.  
{{< highlight json "linenos=inline, hl_lines=3 6-8, style=emacs" >}}
{
    "evt": "se",
    "modules": {
        "Allsky": {
            "properties": {
                "coming": {
                    "elements": {
                        "sunrise": {
                            "autoupdate": false,
                            "badge": false,
                            "directedit": false,
                            "hh": 7,
                            "hint": "",
                            "label": "Prochain lever de Soleil",
                            "mm": 6,
                            "order": "20",
                            "ss": 51,
                            "type": "time",
                            "usems": false
                        },
                        "sunset": {
                            "autoupdate": false,
                            "badge": false,
                            "directedit": false,
                            "hh": 21,
                            "hint": "",
                            "label": "Prochain coucher de Soleil",
                            "mm": 15,
                            "order": "30",
                            "ss": 1,
                            "type": "time",
                            "usems": false
                        }
                    },
                    "enabled": true,
                    "status": 0
                }
            }
        }
    }
}
{{< /highlight >}}
