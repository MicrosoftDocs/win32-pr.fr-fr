---
title: Obtention de l’état d’une fenêtre de capture
description: Obtention de l’état d’une fenêtre de capture
ms.assetid: 5095dbd2-7cd4-48b6-bbb4-1f0bddfcfd06
keywords:
- capGetStatus macro)
- CAPSTATUS, structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8effedac3950f0f57aaa6e57ccd5a93fe3044982c3d6ec6d6bb69b56024a1255
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038369"
---
# <a name="obtaining-the-status-of-a-capture-window"></a>Obtention de l’état d’une fenêtre de capture

L’exemple suivant utilise la fonction [SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos) pour définir la taille de la fenêtre de capture sur les dimensions globales du flux vidéo entrant en fonction des informations retournées par la macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) dans la structure [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) .


```C++
CAPSTATUS CapStatus;

capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS)); 

SetWindowPos(hWndC, NULL, 0, 0, CapStatus.uiImageWidth, 
    CapStatus.uiImageHeight, SWP_NOZORDER | SWP_NOMOVE); 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la capture vidéo](using-video-capture.md)
</dt> </dl>

 

 