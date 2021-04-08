---
title: Affichage des boîtes de dialogue pour définir les caractéristiques de la vidéo
description: Affichage des boîtes de dialogue pour définir les caractéristiques de la vidéo
ms.assetid: 8074f7d1-e8ab-46c3-acc2-a18be0eb4cc7
keywords:
- CAPDRIVERCAPS, structure
- capDriverGetCaps macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73eea12d69a3d23b0345bee3495d32cbb1ad0ffe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840701"
---
# <a name="displaying-dialog-boxes-to-set-video-characteristics"></a><span data-ttu-id="af80f-105">Affichage des boîtes de dialogue pour définir les caractéristiques de la vidéo</span><span class="sxs-lookup"><span data-stu-id="af80f-105">Displaying Dialog Boxes to Set Video Characteristics</span></span>

<span data-ttu-id="af80f-106">Chaque pilote de capture peut fournir jusqu’à trois boîtes de dialogue différentes utilisées pour contrôler les aspects de la numérisation vidéo et du processus de capture.</span><span class="sxs-lookup"><span data-stu-id="af80f-106">Each capture driver can provide up to three different dialog boxes used to control aspects of the video digitization and capture process.</span></span> <span data-ttu-id="af80f-107">L’exemple suivant montre comment afficher ces boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="af80f-107">The following example demonstrates how to display these dialog boxes.</span></span> <span data-ttu-id="af80f-108">Avant d’afficher chaque boîte de dialogue, l’exemple appelle la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) et vérifie la structure [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) retournée pour voir si le pilote de capture peut l’afficher.</span><span class="sxs-lookup"><span data-stu-id="af80f-108">Before displaying each dialog box, the example calls the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro and checks the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure returned to see if the capture driver can display it.</span></span>


```C++
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

CAPDRIVERCAPS CapDriverCaps = { }; 
CAPSTATUS     CapStatus = { };

capDriverGetCaps(hWndC, &CapDriverCaps, sizeof(CAPDRIVERCAPS)); 
 
// Video source dialog box. 
if (CapDriverCaps.fHasDlgVideoSource)
{
    capDlgVideoSource(hWndC); 
}
 
// Video format dialog box. 
if (CapDriverCaps.fHasDlgVideoFormat) 
{
    capDlgVideoFormat(hWndC); 

    // Are there new image dimensions?
    capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS));

    // If so, notify the parent of a size change.
} 
 
// Video display dialog box. 
if (CapDriverCaps.fHasDlgVideoDisplay)
{
    capDlgVideoDisplay(hWndC); 
}
```



## <a name="related-topics"></a><span data-ttu-id="af80f-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="af80f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af80f-110">Utilisation de la capture vidéo</span><span class="sxs-lookup"><span data-stu-id="af80f-110">Using Video Capture</span></span>](using-video-capture.md)
</dt> <dt>

[<span data-ttu-id="af80f-111">**capDriverGetCaps**</span><span class="sxs-lookup"><span data-stu-id="af80f-111">**capDriverGetCaps**</span></span>](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps)
</dt> </dl>

 

 




