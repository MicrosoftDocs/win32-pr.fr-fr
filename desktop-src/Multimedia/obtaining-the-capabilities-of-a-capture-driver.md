---
title: Obtention des fonctionnalités d’un pilote de capture
description: Obtention des fonctionnalités d’un pilote de capture
ms.assetid: 17e90ca6-3646-41cb-8d7a-a2102bc16cc5
keywords:
- Message WM_CAP_DRIVER_GET_CAPS
- capDriverGetCaps macro)
- CAPDRIVERCAPS, structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d15a3b1e01ccff738494f287126b7e1ab033056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509006"
---
# <a name="obtaining-the-capabilities-of-a-capture-driver"></a><span data-ttu-id="18c5f-106">Obtention des fonctionnalités d’un pilote de capture</span><span class="sxs-lookup"><span data-stu-id="18c5f-106">Obtaining the Capabilities of a Capture Driver</span></span>

<span data-ttu-id="18c5f-107">Le message [**WM \_ Cap Driver to Cap \_ \_ \_**](wm-cap-driver-get-caps.md) retourne les fonctionnalités du pilote de capture et du matériel sous-jacent dans la structure [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .</span><span class="sxs-lookup"><span data-stu-id="18c5f-107">The [**WM\_CAP\_DRIVER\_GET\_CAPS**](wm-cap-driver-get-caps.md) message returns the capabilities of the capture driver and underlying hardware in the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span> <span data-ttu-id="18c5f-108">Chaque fois qu’une application connecte un nouveau pilote de capture à la fenêtre de capture, elle doit mettre à jour la structure **CAPDRIVERCAPS** .</span><span class="sxs-lookup"><span data-stu-id="18c5f-108">Each time an application connects a new capture driver to the capture window, it should update the **CAPDRIVERCAPS** structure.</span></span> <span data-ttu-id="18c5f-109">L’exemple suivant utilise la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) pour obtenir les fonctionnalités du pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="18c5f-109">The following example uses the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro to obtain the capture driver capabilities.</span></span>


```C++
CAPDRIVERCAPS CapDrvCaps; 

SendMessage (hWndC, WM_CAP_DRIVER_GET_CAPS, 
    sizeof (CAPDRIVERCAPS), (LONG) (LPVOID) &CapDrvCaps); 

// Or, use the macro to retrieve the driver capabilities. 
// capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 
```



## <a name="related-topics"></a><span data-ttu-id="18c5f-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="18c5f-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18c5f-111">Utilisation de la capture vidéo</span><span class="sxs-lookup"><span data-stu-id="18c5f-111">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




