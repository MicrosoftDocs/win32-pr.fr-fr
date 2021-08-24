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
ms.openlocfilehash: 1453348c52ed8244ac81f830299a632f2fbe9cab03461303d9aa841dcd675666
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497289"
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



 

 




