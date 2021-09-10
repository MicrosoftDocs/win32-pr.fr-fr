---
title: lecture Flux à partir d’un fichier AVI
description: lecture Flux à partir d’un fichier AVI
ms.assetid: fa17cac4-bc6f-48ef-8960-286386b43c82
keywords:
- AVIStreamInfo fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edbea431a5a5f08602b026e26fd15dfe684c555d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363712"
---
# <a name="reading-streams-from-an-avi-file"></a>lecture Flux à partir d’un fichier AVI

La sous-routine suivante obtient des informations de flux à partir d’un fichier AVI et détermine le type de flux à partir de la structure [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) retournée par la fonction [**AVISTREAMINFO**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) .


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



 

 




