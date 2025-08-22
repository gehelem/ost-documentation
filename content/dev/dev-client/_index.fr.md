---
title: Développement client
weight : 20
---

[Voir un exemple de dump complet d'un module](/example.json)

## Modules
Un module est un ensemble de propriétés qui sont dédiées à une tache spécifique (focus/guidage/ ...)
L'identifiant unique du module correspond à son libellé auquel on a supprimé les espaces.  
Il dispose des paramètres suivants :
| Paramètre         | Type      | Description |
|:------------------|:----------|:-------|
|   infos:label      |   string    |   Libellé du module   |
|   infos:name      |   string    |   Nom interne du module   |
|   infos:description      |   string    |   Description du module   |
|   errors      |   array(datetime,string)    |   Tableau des messages d'erreur   |
|   warnings      |   array(datetime,string)    |   Tableau des messages d'alerte   |
|   messages      |   array(datetime,string)    |   Tableau des messages d'information   |
|   globallovs      |   array(string,type,array(type))    |   Liste de valeurs globale   |
|   state      |   N/A    |   N/A   |
## Propriétés
Une propriété est un ensemble d'éléments.
Ces propriétés doivent être représentées hiérarchiquement les unes par rapport aux autres sur le module.
Les valeurs de "level1" et "level2" permettent de déterminer cette hiérarchie.

## Elements
Un élément représente une valeur unique, c'est le niveau le plus bas.  
11 types de valeurs sont possibles :
- int : une valeur entière, qui peut être négative
- float : une valeur décimale, qui peut être négative
- bool : une valeur logique
- string : une chaine de caractères
- date : une date
- time : une heures/minutes/secondes/millisecondes
- img : une image
- video : une vidéo
- light : 4 valeurs possible : standby, ok, warning, erreur
- prg : une barre de progression ou un camembert
- message : un message avec horodatage

{{% notice style="tip" title="Icones"%}}
Les valeurs de paramètre correspondantes à des icones sont celles definies GoogleFonts  
https://fonts.google.com/icons
{{% /notice %}}

### Paramètres systématiques
Ce jeu de paramètres est commun à tous les éléments :
| Paramètre         | Type      | Description |
|:------------------|:----------|:-------|
|   autoupdate      |   bool    |   Ce paramètre n'a pas d'usage pour le frontend   |
|   badge           |   bool    |   Bouton oui/non pour ajouter ou enlever l'éléments dans les favoris   |
|   directedit      |   bool    |   true : la valeur peut être mise à jour directement - false : la valeur doit être mise à jour en même temps que les autres éléments d'une même propriété |
|   hint            |   string  |   Texte explicatif de l'élément, aide à la façon "infobulle"   |
|   label           |   string  |   Libellé de l'élément   |
|   order           |   string  |   Ordre d'affichage de l'élément dans la propriété   |
|   type            |   string  |   Type de valeur - voir liste des valeurs possible ci-dessus   |

### Paramètres optionnels
Ce jeu de paramètres n'est pas défini systématiquement.

| Paramètre         | Type      | Description |
|:------------------|:----------|:-------|
|   posticon        |   string  |   bouton à placer après le libellé de l'élément (voir note icones ci-dessus)    |
|   preicon         |   string  |   bouton à placer avant le libellé de l'élément (voir note icones ci-dessus)    |

### Paramètres spécifiques - int
| Paramètre         | Type      | Description |
|:------------------|:----------|:-------|
|   value           |   int  |   Valeur entière, qui peut être négative   |
|   format           |   string  |   format d'affichage   |
|   listOfValues  |   array(int)  |   Tableau des valeurs autorisées   |
|   globallov  |   string  |   Référence à une liste de valeurs autorisées globale |
|   min           |   int  |   Valeur minimale autorisée   |
|   max           |   int  |   Valeur maximale autorisée   |
|   slider           |   0/1/2  | 0 : Pas de slider - 1 : Slider seulement - 2 : Slider et valeur   |
|   step           |   int  |   Pas du slider   |

### Paramètres spécifiques - float
| Paramètre         | Type      | Description |
|:------------------|:----------|:-------|
|   value           |   float  |   Valeur décimale, qui peut être négative   |
|   format           |   string  |   format d'affichage   |
|   listOfValues  |   array(float)  |   Tableau des valeurs autorisées   |
|   globallov  |   string  |   Référence à une liste de valeurs autorisées globale |
|   min           |   float  |   Valeur minimale autorisée   |
|   max           |   float  |   Valeur maximale autorisée   |
|   slider           |   0/1/2  | 0 : Pas de slider - 1 : Slider seulement - 2 : Slider et valeur   |
|   step           |   float  |   Pas du slider   |

### Paramètres spécifiques - bool
| Paramètre         | Type      | Description |
|:------------------|:----------|:-------|
|   value           |   bool  |   Valeur logique true/false   |
### Paramètres spécifiques - string
| Paramètre         | Type      | Description |
|:------------------|:----------|:-------|
|   value           |   string  |   Valeur alphanumérique   |
|   listOfValues  |   array(string)  |   Tableau des valeurs autorisées   |
|   globallov  |   string  |   Référence à une liste de valeurs autorisées globale |

### Paramètres spécifiques - date
| Paramètre         | Type      | Description |
|:------------------|:----------|:-------|
|   year           |   int  |   Année   |
|   month           |   1-12  |   Mois   |
|   day           |   1-31  |   Jour   |
### Paramètres spécifiques - time
| Paramètre         | Type      | Description |
|:------------------|:----------|:-------|
|   hh           |   0-23  |   Heures   |
|   mm           |   0-59  |   Minutes   |
|   ss           |   0-59  |   Secondes   |
|   ms           |   0-999  |   Millisecondes   |
### Paramètres spécifiques - img
| Paramètre         | Type      | Description |
|:------------------|:----------|:-------|
|   value           |   bool  |   A3   |
### Paramètres spécifiques - video
| Paramètre         | Type      | Description |
|:------------------|:----------|:-------|
|   value           |   bool  |   A3   |
### Paramètres spécifiques - light
| Paramètre         | Type      | Description |
|:------------------|:----------|:-------|
|   value           |   bool  |   A3   |
### Paramètres spécifiques - prg
| Paramètre         | Type      | Description |
|:------------------|:----------|:-------|
|   value           |   bool  |   A3   |
### Paramètres spécifiques - message
| Paramètre         | Type      | Description |
|:------------------|:----------|:-------|
|   value           |   bool  |   A3   |

