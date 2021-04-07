---
title: Comment traiter des messages de notification TrackBar
description: Trackbars notifier la fenêtre parente des actions de l’utilisateur en lui envoyant un \_ message WM HSCROLL ou WM \_ VSCROLL.
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c723ad1bebb5c9f3ec8c4e7aefdc658e0881aef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672205"
---
# <a name="how-to-process-trackbar-notification-messages"></a>Comment traiter des messages de notification TrackBar

Trackbars notifier la fenêtre parente des actions de l’utilisateur en lui envoyant un message [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) .

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="process-trackbar-notification-messages"></a>Traiter les messages de notification TrackBar

L’exemple de code suivant est une fonction qui est appelée lorsque la fenêtre parente de TrackBar reçoit un message [**WM \_ HSCROLL**](wm-hscroll.md) . Dans cet exemple, le TrackBar a le style [**tbs \_ ENABLESELRANGE**](trackbar-control-styles.md) . La position du curseur est comparée à la plage de sélection et le curseur est déplacé vers la position de début ou de fin de la plage de sélection, si nécessaire.


```
// TBNotifications - handles trackbar notifications received 
// in the wParam parameter of WM_HSCROLL. This function simply 
// ensures that the slider remains within the selection range. 

VOID WINAPI TBNotifications( 
    WPARAM wParam,  // wParam of WM_HSCROLL message 
    HWND hwndTrack, // handle of trackbar window 
    UINT iSelMin,   // minimum value of trackbar selection 
    UINT iSelMax)   // maximum value of trackbar selection 
    { 
    DWORD dwPos;    // current position of slider 

    switch (LOWORD(wParam)) { 
    
        case TB_ENDTRACK:
          
            dwPos = SendMessage(hwndTrack, TBM_GETPOS, 0, 0); 
            
            if (dwPos > iSelMax) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMax); 
                    
            else if (dwPos < iSelMin) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMin); 
            
            break; 

        default: 
        
            break; 
        } 
} 
```



## <a name="remarks"></a>Notes

Une boîte de dialogue qui contient un TrackBar de style de type [**tbs \_**](trackbar-control-styles.md) peut utiliser cette fonction lorsqu’elle reçoit un message [**WM \_ VSCROLL**](wm-vscroll.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles TrackBar](using-trackbar-controls.md)
</dt> </dl>

 

 




