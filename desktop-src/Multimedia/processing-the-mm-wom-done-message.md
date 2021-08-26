---
title: Traitement du message de MM_WOM_DONE
description: Traitement du message de fin de \_ WOM mm \_
ms.assetid: 215167d0-3020-453d-b6b3-cee5803836c9
keywords:
- sons Waveform, messages
- audio auxiliaire, messages
- audio Wave, message MM_WOM_DONE
- audio auxiliaire, MM_WOM_DONE message
- Message MM_WOM_DONE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6aca93f23ed74a4a4974633d8345f2e897535e156ccc03f46eb0da92a2d2fdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037859"
---
# <a name="processing-the-mm_wom_done-message"></a>Traitement du message de fin de \_ WOM mm \_

L’exemple suivant montre comment traiter le message [**mm \_ WOM \_ done**](mm-wom-done.md) . Cet exemple suppose que l’application ne lit pas plusieurs blocs de données. elle peut donc fermer le périphérique de sortie après la lecture d’un bloc de données unique.


```C++
// WndProc--Main window procedure. 
LRESULT FAR PASCAL WndProc(HWND hWnd, UINT msg, WPARAM wParam, 
    LPARAM lParam) 
{ 
switch (msg) 
{ 
    case MM_WOM_DONE: 
 
    // A waveform-audio data block has been played and 
    // can now be freed. 
    waveOutUnprepareHeader((HWAVEOUT) wParam, 
        (LPWAVEHDR) lParam, sizeof(WAVEHDR) ); 
    
    // Free hData memory. 
    
    waveOutClose((HWAVEOUT) wParam); 
    break; 
    } 
    return DefWindowProc(hWnd, msg, wParam, lParam); 
} 
```



 

 




