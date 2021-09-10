---
title: Données de dessin
description: Données de dessin
ms.assetid: cc4f383d-54d4-4027-ad6a-da19bb07c17f
keywords:
- Gestionnaire de compression vidéo (VCM), dessin
- VCM (gestionnaire de compression vidéo), dessin
- ICDraw fonction)
- ICDrawStart macro)
- ICDrawStop macro)
- ICDrawFlush macro)
- ICDrawEnd macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f598ef47bbbf6b8f53c7fb2639c9ddff1390ab
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364087"
---
# <a name="drawing-data"></a>Données de dessin

L’exemple suivant utilise la fonction [**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) et les macros [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart), [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop), [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush)et [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) pour dessiner des données à l’écran.


```C++
DWORD    dwNumBuffers; 
 
// Find out how many buffers need filling before drawing starts.

ICGetBuffersWanted(hIC, &dwNumBuffers); 
for (dw = 0; dw < dwNumBuffers; dw++)
{ 
    ICDraw(hIC, 0, lpFormat, lpData, cbData, dw); // fill the pipeline
    
    // Point lpFormat and lpData to next format and buffer.
    
} 
ICDrawStart(hIC);  // starts the clock 
dw = 0; 
while (fPlaying) 
{ 
    ICDraw(hIC, 0, lpFormat, lpData, chData, dw); // fill more buffers 
    
    // Point lpFormat and lpData to next format and buffer,
    // update dw.
} 
 
ICDrawStop(hIC);   // stops drawing and decompressing when done 
ICDrawFlush(hIC);  // flushes any existing buffers 
ICDrawEnd(hIC);    // ends decompression 
 
```



 

 




