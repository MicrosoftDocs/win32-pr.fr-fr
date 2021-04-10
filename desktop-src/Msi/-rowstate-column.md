---
description: Le nom de colonne réservé \_ RowState représente l’état non persistant associé à chaque ligne de table dans une table de base de données de programme d’installation.
ms.assetid: ff570b47-7c16-47ae-b1c2-2ecad9266372
title: _RowState colonne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e61a2964d7d11c1c2429ad95e9de2b8bdb148954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034414"
---
# <a name="_rowstate-column"></a>\_RowState (colonne)

Le nom de colonne réservé \_ RowState représente l’état non persistant associé à chaque ligne de table dans une table de base de données de programme d’installation. La pseudo-colonne est de type [entier](integer.md), et la valeur se compose d’un jeu d’indicateurs binaires. Tous les bits sont lisibles, mais seuls les bits UserInfo et Temporary peuvent être définis. Ces données sont disponibles uniquement tant que les tables sont verrouillées ou en cours d’utilisation (c’est-à-dire qu’une vue contenant les tables existe). Le tableau suivant indique les attributs qu’une ligne peut avoir.



| Nom           | Valeur | Signification                                                        |
|----------------|-------|----------------------------------------------------------------|
| iraUserInfo    | 0x01  | L’attribut est destiné à un usage externe. Cette valeur peut être mise à jour.  |
| iraTemporary   | 0x02  | La ligne n’est pas persistante. Cette valeur peut être mise à jour.          |
| iraModified    | 0x04  | Une ligne a été mise à jour.                                        |
| iraInserted    | 0x08  | Une ligne a été insérée.                                       |
| iraMergeFailed | 0x0F  | Une tentative de fusion avec des données non-clés non-identiques a été effectuée. |



 

Les bits 6 à 8 sont réservés.

 

 



