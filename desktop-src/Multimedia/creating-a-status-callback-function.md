---
title: Création d’une fonction de rappel d’État
description: Création d’une fonction de rappel d’État
ms.assetid: 9aa98340-a5a0-4084-9670-b3c27a1351ed
keywords:
- capSetCallbackOnStatus macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592a5582bca37f644810f3496a39321d22da43be
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367823"
---
# <a name="creating-a-status-callback-function"></a>Création d’une fonction de rappel d’État

L’exemple suivant est une fonction de rappel d’état simple. Inscrivez ce rappel à l’aide de la macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) .


```C++
TCHAR gachAppName[] = TEXT("Application Name");  // Application name.
TCHAR gachBuffer[100];  // Global buffer.

// StatusCallbackProc: status callback function. 
// hWnd:               capture window handle. 
// nID:                status code for the current status. 
// lpStatusText:       status text string for the current status. 
// 
LRESULT PASCAL StatusCallbackProc(HWND hWnd, int nID, 
    LPTSTR lpStatusText) 
{ 
    if (!hWnd) 
        return FALSE; 
 
    if (nID == 0) {
        // Clear old status messages.
        SetWindowText(hWnd, gachAppName); 
        return (LRESULT) TRUE; 
    } 
    // Show the status ID and status text. 
    _stprintf_s(gachBuffer, TEXT("Status# %d: %s"), nID, lpStatusText); 
 
    SetWindowText(hWnd, gachBuffer); 
    return (LRESULT) TRUE; 
} 
 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la capture vidéo](using-video-capture.md)
</dt> </dl>

 

 




