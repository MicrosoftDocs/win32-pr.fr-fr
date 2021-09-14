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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021200"
---
# <a name="determining-if-a-driver-can-handle-the-input-format"></a>Déterminer si un pilote peut gérer le format d’entrée

L’exemple suivant montre comment vérifier le format d’entrée à l’aide de la macro [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) .


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



 

 




