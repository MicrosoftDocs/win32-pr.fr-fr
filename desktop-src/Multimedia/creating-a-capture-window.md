---
title: Création d’une fenêtre de capture
description: Création d’une fenêtre de capture
ms.assetid: a727ce14-9b12-4f21-bab4-fa2eb245dce7
keywords:
- capCreateCaptureWindow fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28375da063839d3120ca60bdabd5ca997fa31b02
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029077"
---
# <a name="creating-a-capture-window"></a><span data-ttu-id="9ef77-104">Création d’une fenêtre de capture</span><span class="sxs-lookup"><span data-stu-id="9ef77-104">Creating a Capture Window</span></span>

<span data-ttu-id="9ef77-105">L’exemple suivant crée une fenêtre de capture à l’aide de la fonction [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa) .</span><span class="sxs-lookup"><span data-stu-id="9ef77-105">The following example creates a capture window by using the [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa) function.</span></span>


```C++
hWndC = capCreateCaptureWindow (
    TEXT("My Capture Window"),   // window name if pop-up 
    WS_CHILD | WS_VISIBLE,       // window style 
    0, 0, 160, 120,              // window position and dimensions
    (HWND) hwndParent, 
    (int) nID /* child ID */); 
```



## <a name="related-topics"></a><span data-ttu-id="9ef77-106">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9ef77-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ef77-107">Utilisation de la capture vidéo</span><span class="sxs-lookup"><span data-stu-id="9ef77-107">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




