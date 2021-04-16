---
title: Ouverture d’un fichier AVI
description: Ouverture d’un fichier AVI
ms.assetid: 322eb45f-7dd3-40f4-b6bf-381021c50397
keywords:
- AVIFileInit fonction)
- AVIFileOpen fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833219194dc984bbf7bfa3d0415f77c5eed9b43b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462223"
---
# <a name="opening-an-avi-file"></a><span data-ttu-id="96e52-105">Ouverture d’un fichier AVI</span><span class="sxs-lookup"><span data-stu-id="96e52-105">Opening an AVI File</span></span>

<span data-ttu-id="96e52-106">L’exemple suivant initialise la bibliothèque AVIFile à l’aide de la fonction [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) et ouvre un fichier AVI à l’aide de la fonction [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) .</span><span class="sxs-lookup"><span data-stu-id="96e52-106">The following example initializes the AVIFile library using the [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) function and opens an AVI file using the [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) function.</span></span> <span data-ttu-id="96e52-107">La fonction utilise un gestionnaire de fichiers par défaut.</span><span class="sxs-lookup"><span data-stu-id="96e52-107">The function uses a default file handler.</span></span>


```C++
// LoadAVIFile - loads AVIFile and opens an AVI file. 
// 
// szfile - filename 
// hwnd - window handle 
// 
VOID LoadAVIFile(LPCSTR szFile, HWND hwnd) 
{ 
    LONG hr; 
    PAVIFILE pfile; 
 
    AVIFileInit();          // opens AVIFile library 
 
    hr = AVIFileOpen(&pfile, szFile, OF_SHARE_DENY_WRITE, 0L); 
    if (hr != 0){ 
        // Handle failure.
        return; 
    } 
 
// 
// Place functions here that interact with the open file. 
// 
 
    AVIFileRelease(pfile);  // closes the file 
    AVIFileExit();          // releases AVIFile library 
} 
 
```



 

 




