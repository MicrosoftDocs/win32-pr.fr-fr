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
# <a name="format-identifieroffset-pair"></a><span data-ttu-id="5924d-103">Couple identificateur de format/décalage</span><span class="sxs-lookup"><span data-stu-id="5924d-103">Format Identifier/Offset Pair</span></span>

<span data-ttu-id="5924d-104">La deuxième partie du flux de propriétés du jeu de propriétés contient une paire identificateur de format/décalage.</span><span class="sxs-lookup"><span data-stu-id="5924d-104">The second part of the property set stream contains one Format Identifier/Offset Pair.</span></span> <span data-ttu-id="5924d-105">FMTID est le nom du jeu de propriétés ; Il identifie de façon unique la manière dont le contenu de la section suivante est interprété.</span><span class="sxs-lookup"><span data-stu-id="5924d-105">The FMTID is the name of the property set; it uniquely identifies how to interpret the contents of the following section.</span></span> <span data-ttu-id="5924d-106">Le décalage est la distance, en octets, entre le début du flux entier et l’emplacement où la section commence.</span><span class="sxs-lookup"><span data-stu-id="5924d-106">The Offset is the distance, in bytes, from the start of the whole stream to where the section begins.</span></span>

<span data-ttu-id="5924d-107">La structure suivante est utile pour gérer les paires identificateur de format/décalage.</span><span class="sxs-lookup"><span data-stu-id="5924d-107">The following structure is helpful in handling Format Identifier/Offset Pairs.</span></span>

``` syntax
typedef struct tagFORMATIDOFFSET 
{ 
    FMTID  fmtid ;     // Name of the section. 
    DWORD  dwOffset ;  // Offset for the section. 
} FORMATIDOFFSET;
```

 

 




