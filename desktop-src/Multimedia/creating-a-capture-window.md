---
title: Création d’une fenêtre de capture
description: Création d’une fenêtre de capture
ms.assetid: a727ce14-9b12-4f21-bab4-fa2eb245dce7
keywords:
- capCreateCaptureWindow fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d44e7701900d090a8d73b226039d468e2da817e9c0f9746fc10eaa13578d5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144772"
---
# <a name="creating-a-capture-window"></a>Création d’une fenêtre de capture

L’exemple suivant crée une fenêtre de capture à l’aide de la fonction [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa) .


```C++
hWndC = capCreateCaptureWindow (
    TEXT("My Capture Window"),   // window name if pop-up 
    WS_CHILD | WS_VISIBLE,       // window style 
    0, 0, 160, 120,              // window position and dimensions
    (HWND) hwndParent, 
    (int) nID /* child ID */); 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la capture vidéo](using-video-capture.md)
</dt> </dl>

 

 




