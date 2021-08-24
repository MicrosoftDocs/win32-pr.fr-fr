---
description: Le nom de colonne réservé \_ RowState représente l’état non persistant associé à chaque ligne de table dans une table de base de données de programme d’installation.
ms.assetid: ff570b47-7c16-47ae-b1c2-2ecad9266372
title: _RowState colonne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e0164b76589dfa76deb8754df3e11a8b8250a43d791dec92d0fee65dfb719b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146092"
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

 

 



