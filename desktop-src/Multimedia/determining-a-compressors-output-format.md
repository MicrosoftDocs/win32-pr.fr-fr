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
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101632"
---
# <a name="determining-a-compressors-output-format"></a><span data-ttu-id="1d49d-108">Détermination du format de sortie d’un compresseur</span><span class="sxs-lookup"><span data-stu-id="1d49d-108">Determining a Compressor's Output Format</span></span>

<span data-ttu-id="1d49d-109">L’exemple suivant utilise la macro [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) size pour déterminer la taille de mémoire tampon nécessaire pour les données qui spécifient le format de compression, alloue une mémoire tampon de la taille appropriée à l’aide de la fonction [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) et récupère les informations de format de compression à l’aide de la macro **ICCompressGetFormat** .</span><span class="sxs-lookup"><span data-stu-id="1d49d-109">The following example uses the [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) size macro to determine the buffer size needed for the data specifying the compression format, allocates a buffer of the appropriate size using the [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) function, and retrieves the compression format information using the **ICCompressGetFormat** macro.</span></span>


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// *lpbiIn must be initialized to the input format. 
 
dwFormatSize = ICCompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICCompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



<span data-ttu-id="1d49d-110">L’exemple suivant utilise la macro [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) pour déterminer si un compresseur peut gérer les formats d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="1d49d-110">The following example uses the [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) macro to determine whether a compressor can handle the input and output formats.</span></span>


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// Both *lpbiIn and *lpbiOut must be initialized to the respective
// formats.
 

if (ICCompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
 
    // Format is supported; use the compressor. 
 
}
 
 
```



<span data-ttu-id="1d49d-111">L’exemple suivant utilise la macro [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) pour déterminer la taille de la mémoire tampon et alloue une mémoire tampon de cette taille à l’aide de [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc).</span><span class="sxs-lookup"><span data-stu-id="1d49d-111">The following example uses the [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) macro to determine the buffer size, and it allocates a buffer of that size using [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc).</span></span>


```C++
// Find the worst-case buffer size. 
dwCompressBufferSize = ICCompressGetSize(hIC, lpbiIn, lpbiOut); 
 
// Allocate a buffer and get lpOutput to point to it. 
h = GlobalAlloc(GHND, dwCompressBufferSize); 
lpOutput = (LPVOID)GlobalLock(h);
 
 
```



 

 