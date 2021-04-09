---
title: Obtention de l’état d’une fenêtre de capture
description: Obtention de l’état d’une fenêtre de capture
ms.assetid: 5095dbd2-7cd4-48b6-bbb4-1f0bddfcfd06
keywords:
- capGetStatus macro)
- CAPSTATUS, structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f848898247ad8ea2ddbb0dde7a13c08b6a7274
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940902"
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

 

 