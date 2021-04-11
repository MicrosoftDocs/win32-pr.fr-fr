---
title: Déterminer si un pilote peut gérer le format d’entrée
description: Déterminer si un pilote peut gérer le format d’entrée
ms.assetid: 456eab43-d830-4a28-b724-3ef35b852372
keywords:
- Video Compression Manager (VCM), format d’entrée
- VCM (Video Compression Manager), format d’entrée
- ICDrawQuery macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b3e2da69f8c061a7d0aefe847f40113d5104d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029193"
---
# <a name="determining-if-a-driver-can-handle-the-input-format"></a><span data-ttu-id="4c68e-106">Déterminer si un pilote peut gérer le format d’entrée</span><span class="sxs-lookup"><span data-stu-id="4c68e-106">Determining If a Driver Can Handle the Input Format</span></span>

<span data-ttu-id="4c68e-107">L’exemple suivant montre comment vérifier le format d’entrée à l’aide de la macro [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) .</span><span class="sxs-lookup"><span data-stu-id="4c68e-107">The following example shows how to check the input format with the [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) macro.</span></span>


```C++
// lpbiIn points to BITMAPINFOHEADER structure indicating the input 
// format. 

if (ICDrawQuery(hIC, lpbiIn) == ICERR_OK) 
{ 
    // Driver recognizes the input format. 
} 
else 
{ 
    // Need a different decompressor. 
} 
 
```



 

 




