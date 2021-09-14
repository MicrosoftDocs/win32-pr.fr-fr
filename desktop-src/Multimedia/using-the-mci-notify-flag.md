---
title: Utilisation de l’indicateur MCI_NOTIFY
description: Utilisation de l' \_ indicateur de notification MCI
ms.assetid: 1d1803c8-f315-463e-ae0d-a258aa3af3c9
keywords:
- Indicateur de MCI_NOTIFY
- Commande MCI_PLAY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472613d2e6efcd6b30c88ed64dfa7875b4742527
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194919"
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



 

 




