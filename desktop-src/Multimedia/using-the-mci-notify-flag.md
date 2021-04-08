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
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839570"
---
# <a name="using-the-mci_notify-flag"></a><span data-ttu-id="3b6e0-105">Utilisation de l' \_ indicateur de notification MCI</span><span class="sxs-lookup"><span data-stu-id="3b6e0-105">Using the MCI\_NOTIFY Flag</span></span>

<span data-ttu-id="3b6e0-106">L’exemple suivant montre comment l' \_ indicateur de notification MCI est utilisé avec la commande [**MCI \_ Play**](mci-play.md) .</span><span class="sxs-lookup"><span data-stu-id="3b6e0-106">The following example shows how the MCI\_NOTIFY flag is used with the [**MCI\_PLAY**](mci-play.md) command.</span></span> <span data-ttu-id="3b6e0-107">Le descripteur de la procédure de fenêtre qui traitera le message [**mm \_ MCINOTIFY**](mm-mcinotify.md) est spécifié dans *HWND*.</span><span class="sxs-lookup"><span data-stu-id="3b6e0-107">The handle to the window procedure that will process the [**MM\_MCINOTIFY**](mm-mcinotify.md) message is specified in *hwnd*.</span></span>


```C++
MCI_DGV_PLAY_PARMS mciPlay; 
DWORD dwFlags; 
 
mciPlay.dwCallback = MAKELONG(hwnd, 0); 
dwFlags = MCI_NOTIFY; 
 
mciSendCommand(wMCIDeviceID, MCI_PLAY, dwFlags, (DWORD)(LPSTR)&mciPlay); 
```



 

 




