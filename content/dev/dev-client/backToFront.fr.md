---
title: Messages en provenance du serveur
weight : 30
---


## moduledump
Un message par module, contenant toutes ses propriétés.  
[exemple](/example.json)

## ap
Mise à jour de toutes les informations d'une propriété donnée.

## se
Mise à jour des valeurs des éléments.  
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
