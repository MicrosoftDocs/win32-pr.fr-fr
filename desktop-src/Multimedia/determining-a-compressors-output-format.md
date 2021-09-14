---
title: Détermination du format de sortie d’un compresseur
description: Détermination du format de sortie d’un compresseur
ms.assetid: 910bd77f-4c65-4ea2-bab2-96f42a2b6cf1
keywords:
- Video Compression Manager (VCM), format de sortie
- VCM (Video Compression Manager), format de sortie
- ICCompressGetFormat macro)
- ICCompressQuery macro)
- ICCompressGetSize macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c4356870598dc08ad84c4073be5ffa3c2ddbd5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021209"
---
# <a name="determining-a-compressors-output-format"></a>Détermination du format de sortie d’un compresseur

L’exemple suivant utilise la macro [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) size pour déterminer la taille de mémoire tampon nécessaire pour les données qui spécifient le format de compression, alloue une mémoire tampon de la taille appropriée à l’aide de la fonction [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) et récupère les informations de format de compression à l’aide de la macro **ICCompressGetFormat** .


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// *lpbiIn must be initialized to the input format. 
 
dwFormatSize = ICCompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICCompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



L’exemple suivant utilise la macro [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) pour déterminer si un compresseur peut gérer les formats d’entrée et de sortie.


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// Both *lpbiIn and *lpbiOut must be initialized to the respective
// formats.
 

if (ICCompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
 
    // Format is supported; use the compressor. 
 
}
 
 
```



L’exemple suivant utilise la macro [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) pour déterminer la taille de la mémoire tampon et alloue une mémoire tampon de cette taille à l’aide de [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc).


```C++
// Find the worst-case buffer size. 
dwCompressBufferSize = ICCompressGetSize(hIC, lpbiIn, lpbiOut); 
 
// Allocate a buffer and get lpOutput to point to it. 
h = GlobalAlloc(GHND, dwCompressBufferSize); 
lpOutput = (LPVOID)GlobalLock(h);
 
 
```



 

 