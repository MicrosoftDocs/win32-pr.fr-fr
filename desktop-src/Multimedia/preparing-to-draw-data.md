---
title: Préparation du dessin des données
description: Préparation du dessin des données
ms.assetid: 98adcee4-06c0-4684-bd9e-e030e3f9a59d
keywords:
- Gestionnaire de compression vidéo (VCM), dessin
- VCM (gestionnaire de compression vidéo), dessin
- ICDrawBegin macro)
- ICDrawEnd macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de20d23c0ded51d1933918c16da3f8827b77f796
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364096"
---
# <a name="preparing-to-draw-data"></a>Préparation du dessin des données

L’exemple suivant illustre la séquence d’initialisation qui indique au décompresseur de dessiner en mode plein écran. Elle utilise les macros [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) et [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) .


```C++
// Assume lpbiIn has the input format, dwRate has the data rate. 

if (ICDrawBegin(hIC, ICDRAW_QUERY | ICDRAW_FULLSCREEN, NULL, NULL, 
    NULL, 0, 0, 0, 0, lpbiIn, 0, 0, 0, 0, dwRate, 
    dwScale) == ICERR_OK) 
{ 
    // Decompressor supports this drawing so set up to draw. 
    ICDrawBegin(hIC, ICDRAW_FULLSCREEN, hPal, NULL, NULL, 0, 0, 0, 
        0, lpbiIn, 0, 0, lbpi->biWidth, lpbi->biHeight, dwRate, 
        dwScale); 
    . 
    . // Start decompressing and drawing frames. 
    . 
 
    // Drawing done. Terminate procedure. 
    ICDrawEnd(hIC); 
} 
else 
{ 
    
    // Use another renderer to draw data on the screen; 
    // ICDraw does not support the format. 
} 
 
```



 

 




