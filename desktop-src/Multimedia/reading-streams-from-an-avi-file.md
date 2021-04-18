---
title: Lecture de flux à partir d’un fichier AVI
description: Lecture de flux à partir d’un fichier AVI
ms.assetid: fa17cac4-bc6f-48ef-8960-286386b43c82
keywords:
- AVIStreamInfo fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edbea431a5a5f08602b026e26fd15dfe684c555d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512022"
---
# <a name="reading-streams-from-an-avi-file"></a><span data-ttu-id="dd5db-104">Lecture de flux à partir d’un fichier AVI</span><span class="sxs-lookup"><span data-stu-id="dd5db-104">Reading Streams from an AVI File</span></span>

<span data-ttu-id="dd5db-105">La sous-routine suivante obtient des informations de flux à partir d’un fichier AVI et détermine le type de flux à partir de la structure [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) retournée par la fonction [**AVISTREAMINFO**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) .</span><span class="sxs-lookup"><span data-stu-id="dd5db-105">The following subroutine obtains stream information from an AVI file and determines the stream type from the [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) structure returned by the [**AVIStreamInfo**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) function.</span></span>


```C++
// StreamTypes - opens the streams in an AVI file and determines 
// stream types. 
// 
// Global variables 
// gcpavi - count of streams in an AVI file 
// gapavi[] = array of stream-interface pointers 
 
void StreamTypes(HWND hwnd) 
{ 
    AVISTREAMINFO     avis; 
    LONG    r, lHeight = 0; 
    WORD    w; 
    int     i; 
    RECT    rc; 
 
// Walk through all streams. 
    for (i = 0; i < gcpavi; i++) { 
        AVIStreamInfo(gapavi[i], &avis, sizeof(avis)); 
 
        if (avis.fccType == streamtypeVIDEO) { 
 
        // Place video-processing functions here. 
 
        } 
        else if (avis.fccType == streamtypeAUDIO) { 
 
        // Place audio-processing functions here. 
 
        } 
        else if (avis.fccType == streamtypeTEXT) { 
 
        // Place text-processing functions here. 
 
        } 
    } 
} 
 
```



 

 




