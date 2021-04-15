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
ms.openlocfilehash: 73e909777c115b6b10500e081a08bde6cfe24b00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462211"
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



 

 




