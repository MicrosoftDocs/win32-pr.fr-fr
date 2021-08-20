---
title: Utilisation de l’indicateur MCI_NOTIFY
description: Utilisation de l' \_ indicateur de notification MCI
ms.assetid: 1d1803c8-f315-463e-ae0d-a258aa3af3c9
keywords:
- Indicateur de MCI_NOTIFY
- Commande MCI_PLAY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b0e7269ee7d80dd47372d9210fbdbc1332b3a88a96e2a17d6719c9945ab30aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136137"
---
# <a name="using-the-mci_notify-flag"></a>Utilisation de l' \_ indicateur de notification MCI

L’exemple suivant montre comment l' \_ indicateur de notification MCI est utilisé avec la commande [**MCI \_ Play**](mci-play.md) . Le descripteur de la procédure de fenêtre qui traitera le message [**mm \_ MCINOTIFY**](mm-mcinotify.md) est spécifié dans *HWND*.


```C++
MCI_DGV_PLAY_PARMS mciPlay; 
DWORD dwFlags; 
 
mciPlay.dwCallback = MAKELONG(hwnd, 0); 
dwFlags = MCI_NOTIFY; 
 
mciSendCommand(wMCIDeviceID, MCI_PLAY, dwFlags, (DWORD)(LPSTR)&mciPlay); 
```



 

 




