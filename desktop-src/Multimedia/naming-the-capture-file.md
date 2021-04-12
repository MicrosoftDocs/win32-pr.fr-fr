---
title: Attribution d’un nom au fichier de capture
description: Attribution d’un nom au fichier de capture
ms.assetid: fae2fd6a-4c2f-432f-a714-9faae6daeafe
keywords:
- capFileSetCaptureFile macro)
- capFileAlloc macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ea091a36777e176124689ba57be6c0fb75d07d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310385"
---
# <a name="naming-the-capture-file"></a><span data-ttu-id="65c61-105">Attribution d’un nom au fichier de capture</span><span class="sxs-lookup"><span data-stu-id="65c61-105">Naming the Capture File</span></span>

<span data-ttu-id="65c61-106">L’exemple suivant utilise la macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) pour spécifier un autre nom de fichier (MYCAP.AVI) pour le fichier de capture et la macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) pour préallouer un fichier de 5 Mo.</span><span class="sxs-lookup"><span data-stu-id="65c61-106">The following example uses the [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) macro to specify an alternate filename (MYCAP.AVI) for the capture file and the [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) macro to preallocate a file of 5 MB.</span></span>


```C++
char szCaptureFile[] = "MYCAP.AVI";

capFileSetCaptureFile( hWndC, szCaptureFile); 
capFileAlloc( hWndC, (1024L * 1024L * 5)); 
 
```



## <a name="related-topics"></a><span data-ttu-id="65c61-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="65c61-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65c61-108">Utilisation de la capture vidéo</span><span class="sxs-lookup"><span data-stu-id="65c61-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




