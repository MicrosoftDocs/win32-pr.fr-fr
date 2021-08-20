---
title: Comportement de substitution de la police HTML
description: Comportement de substitution de la police HTML
ms.assetid: 5BDFBD58-0B34-4A58-BFAF-B8BB1DD569DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eabc2c009657adc9b77775c550244c4bbe6a5a3b8b262c8ce915cab4f9e5756
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117672047"
---
# <a name="html-font-fallback-behavior"></a>Comportement de substitution de la police HTML

## <a name="platform"></a>Plateforme

Clients-* * Windows 8.1  
**serveurs-** Windows Server 2012 R2  


## <a name="description"></a>Description

Microsoft met à jour la logique des polices de l’interface utilisateur pour plusieurs langues dans Windows les applications du windows Store en HTML. Au lieu d’utiliser une police unique pour toutes les langues, la police de l’interface utilisateur est maintenant déterminée en fonction de la langue. Par exemple, les polices de l’interface utilisateur pour le japonais seront désormais Meiryo l’interface utilisateur dans les applications qui utilisent HTML.

## <a name="manifestation"></a>Manifestation

Les applications qui dépendent d’une police ancienne peuvent paraître différentes ; Bien que l’apparence de votre application soit améliorée en général grâce à des polices plus lisibles, il peut y avoir un problème avec les dispositions qui dépendent de la taille de contenu parfait. Par exemple, certaines lignes de contenu peuvent être plus volumineuses qu’elles ne l’étaient auparavant, provoquant des sauts de ligne et/ou un redimensionnement inattendus des éléments de conteneur. Toutefois, dans la pratique, nous n’avons remarqué aucun problème avec les applications existantes.

## <a name="solution"></a>Solution

Les applications affectées peuvent atténuer ce comportement en spécifiant une police donnée via CSS (par exemple, « font-family : Meiryo UI ») au lieu de compter sur les anciennes polices par défaut. Le tableau suivant fournit la police de l’interface utilisateur pour chacun des noms de script.



| Nom du script        | Police de l’interface utilisateur               |
|--------------------|-----------------------|
| Arabe             | Segoe UI              |
| Arménien           | Segoe UI              |
| Bengali            | Nirmala UI            |
| Bopomofo           | Microsoft JhengHei UI |
| Braille            | Segoe UI Symbol       |
| Bugi           | Leelawadee UI         |
| SYLLABE CANADIENNE | Gadugi                |
| Cherokee           | Gadugi                |
| Copte             | Segoe UI Symbol       |
| Han (simplifié)   | Microsoft YaHei UI    |
| Han (traditionnel)  | Microsoft JhengHei UI |
| Cyrillique           | Segoe UI              |
| Dévanâgarî         | Nirmala UI            |
| Deseret            | Segoe UI Symbol       |
| Éthiopien           | Ebrima                |
| Géorgien           | Segoe UI              |
| Lettre         | Segoe UI Symbol       |
| La             | Segoe UI Symbol       |
| Grec              | Segoe UI              |
| Goudjrati           | Nirmala UI            |
| Gurmukhi           | Nirmala UI            |
| Hébreu             | Segoe UI              |
| Ancien italique         | Segoe UI Symbol       |
| Javanais           | Texte javanais         |
| Japonais           | Interface utilisateur Meiryo             |
| Kannada            | Interface utilisateur Mirmala            |
| Khmer              | Leelawadee UI         |
| Coréen             | Malgun Gothic         |
| Lao                | Leelawadee            |
| Latin              | Segoe UI              |
| Malayalam          | Nirmala UI            |
| Mongol          | Mongolian Baiti       |
| Myanmar            | Myanmar Text          |
| N’ko               | Ebrima                |
| OGAM              | Segoe UI Symbol       |
| Ol tchiki           | Nirmala UI            |
| Ancien turc         | Segoe UI Symbol       |
| Odia              | Nirmala UI            |
| Osmanya            | Ebrima                |
| PHAGS-PA           | Microsoft PhagsPa     |
| Lettre              | Segoe UI Symbol       |
| Sora Sompeng       | Nirmala UI            |
| Cingalais            | Nirmala UI            |
| Syriaque             | Estrangelo Edessa     |
| LETTRE TAÏ le             | Microsoft Tai Le      |
| Nouveau taï lü        | Microsoft New Tai Lue |
| Tamoul              | Nirmala UI            |
| Télougou             | Nirmala UI            |
| Tifinagh           | Ebrima                |
| Tana             | MV Boli               |
| Thaï               | Leelawadee UI         |
| Tibétain            | Microsoft Himalaya    |
| Vaï                | Ebrima                |
| Yi                 | Microsoft Yi Baiti    |



 

 

 




