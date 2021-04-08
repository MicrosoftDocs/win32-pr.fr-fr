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
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101573"
---
# <a name="determining-a-decompressors-output-format"></a><span data-ttu-id="15180-108">Détermination du format de sortie d’un décompresseur</span><span class="sxs-lookup"><span data-stu-id="15180-108">Determining a Decompressor's Output Format</span></span>

<span data-ttu-id="15180-109">L’exemple suivant détermine la taille de la mémoire tampon nécessaire pour les données qui spécifient le format de décompression à l’aide de la macro [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) , alloue une mémoire tampon de la taille appropriée à l’aide de la fonction [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) et récupère les informations de format de décompression à l’aide de la macro [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) .</span><span class="sxs-lookup"><span data-stu-id="15180-109">The following example determines the buffer size needed for the data specifying the decompression format using the [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) macro, allocates a buffer of the appropriate size using the [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) function, and retrieves the decompression format information using the [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) macro.</span></span>


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
 
// Assume *lpbiIn points to the input (compressed) format. 
dwFormatSize = ICDecompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICDecompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



<span data-ttu-id="15180-110">L’exemple suivant montre comment une application peut utiliser la macro [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) pour déterminer si un décompresseur peut gérer les formats d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="15180-110">The following example shows how an application can use the [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) macro to determine if a decompressor can handle the input and output formats.</span></span>


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
// Assume *lpbiIn & *lpbiOut are initialized to the respective 
// formats.
 
if (ICDecompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    
    // Format is supported - use the decompressor. 
    
} 
 
```



<span data-ttu-id="15180-111">Le fragment de code suivant montre comment récupérer les informations de palette à l’aide de la macro [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) .</span><span class="sxs-lookup"><span data-stu-id="15180-111">The following code fragment shows how to get the palette information using the [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) macro.</span></span>


```C++
ICDecompressGetPalette(hIC, lpbiIn, lpbiOut); 
 
// Move up to the palette. 
lpPalette = (LPBYTE)lpbiOut + lpbi->biSize;
 
 
```



 

 