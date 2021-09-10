---
title: Création d’une fonction de rappel de frame
description: Création d’une fonction de rappel de frame
ms.assetid: 37002ee0-9907-4aab-93cc-50fe9cd21cff
keywords:
- capSetCallbackOnFrame macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b2a921bfae235c50387c41865c44bb69b5c05a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367812"
---
# <a name="creating-a-frame-callback-function"></a>Création d’une fonction de rappel de frame

L’exemple suivant est une fonction de rappel d’image simple. Inscrivez ce rappel à l’aide de la macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) .


```
TCHAR gachBuffer[100];  // Global buffer.
DWORD gdwFrameNum = 0;

// FrameCallbackProc: frame callback function. 
// hWnd:              capture window handle. 
// lpVHdr:            pointer to structure containing captured 
//                        frame information. 
// 
LRESULT PASCAL FrameCallbackProc(HWND hWnd, LPVIDEOHDR lpVHdr) 
{ 
    if (!hWnd) 
        return FALSE; 
 
    _stprintf_s(gachBuffer, TEXT("Preview frame# %ld "), gdwFrameNum++); 
    SetWindowText(hWnd, gachBuffer); 
    return (LRESULT) TRUE ; 
} 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la capture vidéo](using-video-capture.md)
</dt> </dl>

 

 




