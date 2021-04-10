---
title: Couple identificateur de format/décalage
description: La deuxième partie du flux de propriétés du jeu de propriétés contient une paire identificateur de format/décalage.
ms.assetid: cc3a748d-e81c-45da-b04f-ea986158a4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f80a85175278b92fedbfd7b2d50d94007b7e4a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309810"
---
# <a name="format-identifieroffset-pair"></a>Couple identificateur de format/décalage

La deuxième partie du flux de propriétés du jeu de propriétés contient une paire identificateur de format/décalage. FMTID est le nom du jeu de propriétés ; Il identifie de façon unique la manière dont le contenu de la section suivante est interprété. Le décalage est la distance, en octets, entre le début du flux entier et l’emplacement où la section commence.

La structure suivante est utile pour gérer les paires identificateur de format/décalage.

``` syntax
typedef struct tagFORMATIDOFFSET 
{ 
    FMTID  fmtid ;     // Name of the section. 
    DWORD  dwOffset ;  // Offset for the section. 
} FORMATIDOFFSET;
```

 

 




