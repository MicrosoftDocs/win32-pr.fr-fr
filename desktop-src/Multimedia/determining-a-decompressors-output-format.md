---
title: Détermination du format de sortie d’un décompresseur
description: Détermination du format de sortie d’un décompresseur
ms.assetid: afedef5e-a506-40bd-aaad-fd85b0468ed7
keywords:
- Video Compression Manager (VCM), format de sortie
- VCM (Video Compression Manager), format de sortie
- ICDecompressGetFormatSize macro)
- ICDecompressQuery macro)
- ICDecompressGetPalette macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb4140a4118cb2a36ccd75088556c53c55fdcb
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364080"
---
# <a name="determining-a-decompressors-output-format"></a>Détermination du format de sortie d’un décompresseur

L’exemple suivant détermine la taille de la mémoire tampon nécessaire pour les données qui spécifient le format de décompression à l’aide de la macro [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) , alloue une mémoire tampon de la taille appropriée à l’aide de la fonction [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) et récupère les informations de format de décompression à l’aide de la macro [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) .


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
 
// Assume *lpbiIn points to the input (compressed) format. 
dwFormatSize = ICDecompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICDecompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



L’exemple suivant montre comment une application peut utiliser la macro [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) pour déterminer si un décompresseur peut gérer les formats d’entrée et de sortie.


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
// Assume *lpbiIn & *lpbiOut are initialized to the respective 
// formats.
 
if (ICDecompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    
    // Format is supported - use the decompressor. 
    
} 
 
```



Le fragment de code suivant montre comment récupérer les informations de palette à l’aide de la macro [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) .


```C++
ICDecompressGetPalette(hIC, lpbiIn, lpbiOut); 
 
// Move up to the palette. 
lpPalette = (LPBYTE)lpbiOut + lpbi->biSize;
 
 
```



 

 