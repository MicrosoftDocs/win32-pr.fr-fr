---
title: Ouverture de la fenêtre de lecture
description: Ouverture de la fenêtre de lecture
ms.assetid: 180f3fb9-cdcb-49ec-a708-84a597295b2f
keywords:
- Commande MCI_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6ea203c3a5d36ab747632b18b6550a3a0319159
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413871"
---
# <a name="opening-the-playback-window"></a>Ouverture de la fenêtre de lecture

L’exemple suivant montre comment utiliser la commande [**MCI \_ Open**](mci-open.md) pour définir une fenêtre parente et créer un enfant de cette fenêtre.


```C++
MCI_DGV_OPEN_PARMS    mciOpen; 
 
mciOpen.lpstrElementName = lpstrFile;  // Set the filename.
mciOpen.dwStyle = WS_CHILD;            // Set the style. 
mciOpen.hWndParent = hWnd;             // Give a window handle. 
 
if (mciSendCommand(0, MCI_OPEN, 
   (DWORD)(MCI_OPEN_ELEMENT|MCI_DGV_OPEN_PARENT|MCI_DGV_OPEN), 
   (DWORD)(LPSTR)&mciOpen) == 0)
{ 
    // Open operation is successful. Continue. 
} 
```



 

 




